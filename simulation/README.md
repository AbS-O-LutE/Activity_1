# Blinky Project In Action

## ON (Both the input are low)

## OFF (One input high and one low)

## OFF (One input high and one low)

## OFF (Both the input are high)

## Code 
```
	for(;;)
    {
        if((!(PINB & (1<<PB0))) && (!(PINC & (1<<PC0))))
    {
        change_led_state(LED_ON);
		delay_ms(LED_ON_TIME);
    }

    else if((!(PINB & (1<<PB0))) && ((PINC & (1<<PC0))))
    {
        change_led_state(LED_OFF);
		delay_ms(LED_OFF_TIME);
    }

    else if(((PINB & (1<<PB0))) && (!(PINC & (1<<PC0))))
    {
        change_led_state(LED_OFF);
		delay_ms(LED_OFF_TIME);
    }

    else if(((PINB & (1<<PB0))) && ((PINC & (1<<PC0))))
        {
            change_led_state(LED_OFF);
		delay_ms(LED_OFF_TIME);
    }

    }
```