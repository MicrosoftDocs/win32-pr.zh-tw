---
description: Windows 7 和 Windows Server 2008 R2 包含服務的下列全新和更新的程式設計項目。
ms.assetid: 4be7e244-ad4c-440d-b04e-23afb4c7ddf2
title: Windows 7 的服務有哪些新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e55cf7aae33522f141fbac68b727842b3dd2fbde21ba97fa46407cf8af6c2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966636"
---
# <a name="whats-new-in-services-for-windows-7"></a>Windows 7 服務的新功能

Windows 7 和 Windows Server 2008 R2 包含服務的下列全新和更新的程式設計項目。

## <a name="new-capabilities"></a>新功能

當觸發程式事件發生時，可以註冊以啟動或停止服務。 這樣就不需要在系統啟動時啟動服務，或讓服務輪詢或主動等候事件;服務可以在需要時啟動，而不是在是否有要執行的工作時自動啟動。 如需詳細資訊，請參閱 [服務觸發程式事件](service-trigger-events.md)。

## <a name="updated-functions"></a>已更新函式



| 函式                                                        | 描述                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)<br/>   | 變更服務的設定參數。 此函數支援受管理的服務帳戶和虛擬帳戶。 如需詳細資訊，請參閱 [服務帳戶的逐步指南](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10))。<br/>                                      |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)<br/> | 變更服務的選擇性設定參數。 此函數支援處理器群組和服務觸發程式事件的新設定資訊層級。<br/>                                                                                                        |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)<br/>               | 建立服務物件，並將它加入至指定的服務控制管理員資料庫。 此函數支援受管理的服務帳戶和虛擬帳戶。 如需詳細資訊，請參閱 [服務帳戶的逐步指南](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10))。<br/> |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                       | 搭配 [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) 函式使用的應用程式定義回呼函數。 這個回呼函式支援對系統時間變更和服務觸發程式事件進行新的擴充控制程式代碼。<br/>                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)<br/>   | 抓取服務的選擇性設定參數。 此函數支援處理器群組和服務觸發程式事件的新設定資訊層級。<br/>                                                                                                      |
| [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)<br/>         | 更新呼叫服務的服務控制管理員的狀態資訊。 此函式支援系統時間變更和服務觸發程式事件的新擴充控制程式代碼。<br/>                                                                                         |



 

## <a name="new-structures"></a>新結構



| 結構                                                                                       | 描述                                                            |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**服務 \_ TIMECHANGE \_ 資訊**](/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info)<br/>                         | 包含系統時間變更設定。 <br/>                      |
| [**服務 \_ 觸發程式**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)<br/>                                          | 表示服務觸發程式事件。<br/>                         |
| [**服務 \_ 觸發程式 \_ 資訊**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)<br/>                               | 包含服務的觸發程式事件資訊。<br/>           |
| [**服務 \_ 觸發程式的 \_ 特定 \_ 資料項目 \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | 包含服務觸發程式事件的觸發程式特定資料。<br/> |



 

 

