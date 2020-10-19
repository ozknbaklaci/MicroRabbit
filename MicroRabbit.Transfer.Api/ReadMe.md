Migrations => Package Manager Console => Default Project => MicroRabbit.Transfer.Data => Add-Migration "Initial Migration" -Context TransferDbContext  ERROR =>  Unable to create an object of type 'BankingDbContext'. For the different patterns supported at design time, see https://go.microsoft.com/fwlink/?linkid=851728
ERROR => Your startup project 'MicroRabbit.Transfer.Api' doesn't reference Microsoft.EntityFrameworkCore.Design. This package is required for the Entity Framework Core Tools to work. Ensure your startup project is correct, install the package, and try again
ERROR => An error occurred while accessing the Microsoft.Extensions.Hosting services. Continuing without the application service provider. Error: Some services are not able to be constructed (Error while validating the service descriptor 'ServiceType: MicroRabbit.Domain.Core.Bus.IEventBus Lifetime: Transient ImplementationType: MicroRabbit.Infra.Bus.RabbitMQBus': Unable to resolve service for type 'MediatR.IMediator' while attempting to activate 'MicroRabbit.Infra.Bus.RabbitMQBus'.)
Unable to create an object of type 'TransferDbContext'. For the different patterns supported at design time, see https://go.microsoft.com/fwlink/?linkid=851728 

ÇÖZÜM => Api projesine Microsoft.EntityFrameworkCore.Design ve Microsoft.EntityFrameworkCore.Tools paketlerini kur,

Sorun devam ederse IoC içinde Account ile ilgili servisleri vs yorum satırına al sonra komutu tekrar çalıştır.

Database => Update-Database -Context TransferDbContext

Yorum satırına alınanları tekrar açabiliriz.


