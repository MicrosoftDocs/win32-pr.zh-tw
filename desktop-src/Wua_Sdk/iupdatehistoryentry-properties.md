---
description: IUpdateHistoryEntry 介面會定義下列屬性。
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: IUpdateHistoryEntry 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3acdc9ed32c35028a253944d434c23231c5b6d
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/11/2021
ms.locfileid: "106986719"
---
# <a name="iupdatehistoryentry-properties"></a>IUpdateHistoryEntry 屬性

[**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)介面會定義下列屬性。



| 屬性                                                               | 描述                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | 取得處理更新之用戶端應用程式的識別碼。                                                  |
| [**日期**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | 取得套用更新的日期和時間。                                                                        |
| [**描述**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | 取得更新的描述。                                                                                       |
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | 取得在更新時從作業傳回的 **HRESULT** 值。                                             |
| [**操作**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | 取得 [**character**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) 值，這個值會指定更新的作業。                      |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | 取得 [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) 值，這個值會指定更新的作業結果。 |
| [**Serverselection.sqlpolicy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | 取得 [**serverselection.sqlpolicy**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) 值，指出提供更新的伺服器。                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | 取得不是 Windows update 之更新服務的服務識別碼。                                           |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | 取得更新的語言特定支援資訊的超連結。                                             |
| [**標題**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | 取得更新的標題。                                                                                             |
| [**UninstallationNotes**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | 取得更新的卸載附注。                                                                              |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | 取得包含更新之卸載步驟的 [**IStringCollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) 介面。  |
| [**UnmappedResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | 取得在更新時從作業傳回的未對應結果碼。                                           |
| [**UpdateIdentity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | 取得字串。 字串包含更新的唯一識別碼。                                                   |



 

 

 
