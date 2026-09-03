# Shree Shyam Courier Portal v2

Ready starter website for Shree Shyam Courier International & Domestic.

## Demo
Open index.html and test:
- SSK100001 = In Transit
- SSK100002 = Delivered

## Production architecture
Customer -> Website -> Secure Backend -> Multi-carrier Tracking API -> Carrier systems
                                   <- Webhooks / refresh

For true universal tracking, connect a multi-carrier provider (for example AfterShip) or individual carrier APIs. The provider/API credentials must be created by the business owner and stored as backend secrets.

## Production database
shipments: internal_awb, carrier, carrier_tracking_no, customer, origin, destination, status, timestamps
tracking_events: shipment_id, status, description, location, event_time
customers: name, phone, email
rate_cards: carrier, service, zone, weight range, customer rate, reseller rate
users: name, email, password_hash, role

## Next deployment steps
1. Buy a domain.
2. Choose HTTPS hosting.
3. Deploy frontend + backend.
4. Create PostgreSQL database.
5. Connect carrier/multi-carrier API.
6. Add secure admin authentication.
7. Configure webhooks and scheduled tracking refresh.
8. Add booking, AWB, invoice, labels, payments and notifications.
