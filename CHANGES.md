# 5.7.0
* Fixed a wrong information in README.md regarding SQL Server compatibility (thanks to @domagojmedo).
* Fixed bug #382 System.FormatExceotion due to invalid format strings when using SelfLog (thanks to @sommmen)
* New sink option to configure tenant when using Azure managed identities (thanks to @mattosaurus).
* Updated .NET target frameworks (obsolete .NET Core 2.0 and 2.1, added .NET Core 3.1 LTS).

# 5.6.1
* Added support for reserved columns (thanks to @susanneschuster).
* Fixes in README.

# 5.6.0
* Fixed issue #191: Added option `EagerlyEmitFirstEvent` by implementing new PeriodicBatchingSink API.
* Replaced `SinkOptions` with `MSSqlServerSinkOptions` and cleaned up namespaced (thanks to @jonorossi for the contribution).
* Target .NET Core 2.1 (LTS) instead of 2.2
* Fixed issue #312: Data conversion issue causes logging to silently fail.

# 5.5.1
* Fixed issue #300 Support DateTime2 data type for TimeStamp column (thanks to @stedel for the contribution).
* Added Sourcelink support and publish symbols to nuget.org which allows consumers of the package to debug into the sink code.
* Added troubleshooting tip in README with workaround for SqlClient issue regarding missing Microsoft.Data.SqlClient.Sni.dll in .NET Framework apps and updated `samples\AppConfigDemo` accordingly.
* Added information in README about batched sink SqlBulkCopy behavior according to issue #209.

# 5.5.0
* Implemented enhancement #208: use Microsoft.Data.SqliClient for all platforms except net452 to enable Column Encryption (thanks to @mungk for the contribution).
* Fixed issue #290 MissingMethodException with .NET Standard 2.0.
* Added .NET Standard 2.0 sample program.
* Minor bug fixes.
* Completed overall refactoring and added unit tests for all refactored code.

# 5.4.0
* Added support for Azure Managed Identities for Resources authentication (thanks to @darrenschwarz for the contribution).
* New interface using `SinkOptions` parameter. Marked old interfaces obsolete.
* Implemented Enhancement #182: configurable property names for custom columns (thanks to @rocknet for the contribution).
* Lots of refactoring and new unit tests.

# 5.3.0  
Code quality release.
 * Added code analysis and editorconfig rules based on Microsoft standards.
 * Fixed code analysis errors where possible and added justified suppressions the few remainig.
 * Use Visual Studio 2019 for AppVeyor builds
 * Updated some dependencies.
 * Added CombinedConfigDemo sample program showing how to combine config and code based sink intitialization.
 * Added a lot of unit tests.

# 5.2.0
 * Enhancement #232: Allow to override formatter for rendering LogEvent column.
 * Fixed #187 (again - still an exception when using logevent column with TimeStamp column type DateTimeOffset).
 * Added sample programs

# 5.1.4
 * Fixed #187 Support datetimeoffset as a column type for default column TimeStamp.
 * Fixed #229 Slight issue with documentation.

# 5.1.3
 * Support binary data type, support specify data length in column config, support specify allow null column
 * Also build on unit-test commits
 * Added issue templase
 * Hybrid config implementation
 * Bugfixes

# 5.1.2
 * Support for Audit sink added (#118/#110).

# 4.0.0
 * Serilog 2.0
 * [Documentation fix](https://github.com/serilog/serilog-sinks-mssqlserver/pull/32)

# 2.0.33
 * Option added to exclude redundant properties from serialized JSON in column LogEvent. (https://github.com/serilog/serilog-sinks-mssqlserver/pull/27)

# 2.0.32
 * Safe conversion of data types. Also included selflog for bulk operation errors. (https://github.com/serilog/serilog-sinks-mssqlserver/pull/4)

# 2.0.31
 * Added the ability to configure additional columns via XML configuration (https://github.com/serilog/serilog-sinks-mssqlserver/pull/6)

# 2.0.30
 * You can optionally save the log event inside the database too. Also added ability to exclude the properties if they are saved already inside additional columns. (https://github.com/serilog/serilog-sinks-mssqlserver/pull/7)

# 2.0.28
 * Added explicit column mappings (https://github.com/serilog/serilog-sinks-mssqlserver/pull/10) 

# 2.0.27
 * Option added to automatically create a database table (by Kiran Varsani (https://github.com/varsanikp))

# 2.0.13
 * Ability to add additional properties as columns in the database

# 2.0.1
 * Option to [write times in UTC](https://github.com/serilog/serilog-sinks-mssqlserver/pull/1)

# 1.5
 * Moved from serilog/serilog
