# mist-cloud-comm

This repository contains the message definition used for Mist message
transport over AMQP by the Mist daemon and any services directly
communicating with Mist devices. The transport uses Protocol Buffer
(proto3) for encoding the messages. See the mist.proto file for details.

## Addressing

Messages are addressed using the endpoint EUI64 addresses and the
message flow can be directed in certain conditions using the
EUI64 addresses of gateways. Local addressing and address resolution
is delegated to the any edge (fog) daemons / gateways / border routers.

## Extended AMID

The Mist AMID concept derives from the TinyOS Active Message ID, which
is an 8-bit value. This has been extended to include the TinyOS message
identifier 0x3F as a prefix, with the goal of opening up the rest of
the 16-bit space in the future, as other protocols and tools are extended.

## Extended AM Group ID

The Mist Group ID concept derives from the TinyOS Active Message Group ID,
which itself relies on the 802.15.4 PAN ID, however, exposes only 8-bits
of the original 16-bit value. The Group ID has been extended with a 0 prefix,
with the goal of opening up the rest of the 16-bit space in the future,
as other protocols and tools are extended.
