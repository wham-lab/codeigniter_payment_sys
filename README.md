
Установка
============


$this->load->library('payments');
$this->ci->load->config('payments');

Примеры
========

Платежи
------------------

### Платеж через PayPal


`
    $this->session->set_userdata(array('payment_type' => 'recurring', 'payment_system' => 'paypal'));
`

Парамерты:

- Credit card type
- Credit card number
- Expire month (mm)
- Expire year (yyyy)
- First name
- Last name
- Billing period (month or year)
- Billing frequency (how many billing cycles during the period)
- Amount
- Max times a payment can fail before the subscription is invalidated.

`
    $payment = $this->payments->make_payment(array('visa', '2039923394027162', '051989', 'Calvin', 'Froedge', gmdate("c"), 'month', '1', '30.00', '3'), false);
`

