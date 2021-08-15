---
description: 服務會使用或執行下列函式。
ms.assetid: 63666848-cbac-4853-8b91-89303f9854c0
title: 服務功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55553e29b2ae9fb8e60db2f421fd8aa68cee1c6b79542c7d3d61ef5bcef490f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888960"
---
# <a name="service-functions"></a>服務功能

服務會使用或執行下列函式。



| 函式                                                             | 描述                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**處理常式**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)                                           | 搭配 [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) 函式使用的應用程式定義回呼函數。     |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)                                       | 搭配 [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) 函式使用的應用程式定義回呼函數。 |
| [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     | 註冊函式以處理服務控制要求。                                                                              |
| [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) | 註冊函式以處理擴充的服務控制要求。                                                                     |
| [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)                                   | 應用程式定義的函式，作為服務的起點。                                                      |
| [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits)                             | 使用服務控制管理員和伺服器服務來註冊服務類型。                                                     |
| [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)                         | 更新呼叫服務的服務控制管理員的狀態資訊。                                                     |
| [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)     | 將服務進程的主要執行緒連接到服務控制管理員。                                                         |



 

控制、設定或與服務互動的程式會使用下列函式。



| 函式                                                                 | 描述                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)                       | 變更服務的設定參數。                                                                                          |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)                     | 變更服務的選擇性設定參數。                                                                                 |
| [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)                         | 關閉服務控制管理員物件或服務物件的指定控制碼。                                                        |
| [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)                                 | 將控制項程式碼傳送至服務。                                                                                                          |
| [**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)                             | 將控制項程式碼傳送至服務。                                                                                                          |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)                                   | 建立服務物件，並將它加入至指定的服務控制管理員資料庫。                                                     |
| [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice)                                   | 從服務控制管理員資料庫標示要刪除的指定服務。                                                         |
| [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa)                   | 抓取相依于指定服務之每個服務的名稱和狀態。                                                        |
| [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)                     | 根據指定的資訊層級，列舉指定的服務控制管理員資料庫中的服務。                             |
| [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)                   | 抓取指定服務的顯示名稱。                                                                                        |
| [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea)                           | 捕獲指定服務的服務名稱。                                                                                        |
| [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                 | 將開機狀態報表給服務控制管理員。                                                                                     |
| [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea)           | 讓應用程式在指定的服務建立或刪除或其狀態變更時接收通知。                 |
| [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)                                   | 在指定的電腦上建立與服務控制管理員的連接，然後開啟指定的服務控制管理員資料庫。 |
| [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)                                       | 開啟現有的服務。                                                                                                                  |
| [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga)                         | 抓取指定服務的設定參數。                                                                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)                       | 抓取指定服務的選擇性設定參數。                                                                   |
| [**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation) | 抓取與目前服務啟動相關的動態資訊。                                                                         |
| [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)    | 捕獲與服務物件相關聯之安全描述項的複本。                                                               |
| [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)                     | 根據指定的資訊層級，抓取指定服務的目前狀態。                                             |
| [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity)        | 設定服務物件的安全描述項。                                                                                           |
| [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)                                     | 啟動服務。                                                                                                                           |



 

## <a name="obsolete-functions"></a>過時的函式

下列函式已過時。<dl>

[**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa)  
[**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)  
[**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)  
[**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)  
[**UnlockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-unlockservicedatabase)  
</dl>

 

 
