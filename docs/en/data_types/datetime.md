<a name="data_type-datetime"></a>

# DateTime

Date with time. Stored in four bytes as a Unix timestamp (unsigned). Allows storing values in the same range as for the Date type. The minimal value is output as 0000-00-00 00:00:00.
The time is stored with accuracy up to one second (without leap seconds).

## Time Zones

The date with time is converted from text (divided into component parts) to binary and back, using the system's time zone at the time the client or server starts. In text format, information about daylight savings is lost.

By default, the client switches to the timezone of the server when it connects. You can change this behavior by enabling the client command-line option `--use_client_time_zone`.

So when working with a textual date (for example, when saving text dumps), keep in mind that there may be ambiguity during changes for daylight savings time, and there may be problems matching data if the time zone changed.


[Original article](https://clickhouse.yandex/docs/en/data_types/datetime/) <!--hide-->
