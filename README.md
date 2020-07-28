# ticket-booking-service
bus ticket booking services

To get seat   -   http://localhost:3939/ticket-booking-service/v1/venue/seats
Seat by id    -   http://localhost:3939/ticket-booking-service/v1/venue/seats/3
Hold          -   http://localhost:3939/ticket-booking-service/v1/venue/seats/hold 
Input Sample
{
    "numSeats":"6250",
    "customerEmail":"koushal10@gmail.com",
    "minLevel":"1",
    "maxLevel":"4"
}

Output
{
    "id": 3,
    "customerEmail": "koushal10@gmail.com",
    "seatHoldVenueDetailList": [
        {
            "level": 1,
            "numberOfSeatHolds": 1250
        },
        {
            "level": 2,
            "numberOfSeatHolds": 500
        },
        {
            "level": 3,
            "numberOfSeatHolds": 1500
        },
        {
            "level": 4,
            "numberOfSeatHolds": 1500
        }
    ]
}


To reserve seat    -   http://localhost:3939/ticket-booking-service/v1/venue/seats/reserve
Input Sample
{
	"seatHoldId":"3",
	"customerEmail":"koushal10@gmail.com"
}


Output Sample
{
    "seatHoldId": 3,
    "customerEmail": "koushal10@gmail.com",
    "confirmationCode": "388d0132-ee95-4328-9414-406f0cb6b3c1"
}
