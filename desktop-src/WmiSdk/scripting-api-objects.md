---
description: 適用于 WMI 的腳本 API 參考描述每個使用特定語法的腳本物件。 如需此語法的說明，請參閱腳本 API 的檔慣例。
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: 腳本 API 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30d3269b137686472f54cdb8cf53720b4aad978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192074"
---
# <a name="scripting-api-objects"></a>腳本 API 物件

適用于 WMI 的腳本 API 參考描述每個使用特定語法的腳本物件。 如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

下表列出 WMI 腳本物件和其使用方式。



| Object                                               | 描述                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | 結構和剖析 CIM [datetime](date-and-time-format.md) 值。                                                                                                                                                                                 |
| [**SWbemEventSource**](swbemeventsource.md)         | 與 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)一起抓取事件。                                                                                                                               |
| [**SWbemLastError**](swbemlasterror.md)             | 當發生錯誤時，提供延伸的錯誤資訊。                                                                                                                                                                                              |
| [**Wbemscripting.swbemlocator**](swbemlocator.md)                 | 取得 [**SWbemServices**](swbemservices.md) 物件，該物件可以存取特定主機電腦上的 WMI。                                                                                                                                     |
| [**SWbemMethod**](swbemmethod.md)                   | 包含單一 WMI 方法定義。                                                                                                                                                                                                               |
| [**SWbemMethodSet**](swbemmethodset.md)             | 取得 [**SWbemMethod**](swbemmethod.md) 物件的集合。                                                                                                                                                                                       |
| [**SWbemNamedValue**](swbemnamedvalue.md)           | 包含單一的名稱值。                                                                                                                                                                                                                         |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md)     | 取得 [**SWbemNamedValue**](swbemnamedvalue.md) 物件集合的存取權。                                                                                                                                                                     |
| [**SWbemObject**](swbemobject.md)                   | 包含和操作單一 WMI 物件類別或實例。                                                                                                                                                                                        |
| [**SWbemObjectEx**](swbemobjectex.md)               | 擴充 [**SWbemObject**](swbemobject.md)的功能。 這個物件會加入 [**SWbemRefresher**](swbemrefresher.md)物件的 [**Refresh**](swbemrefresher-refresh.md)方法。                                                           |
| [**SWbemObjectPath**](swbemobjectpath.md)           | 產生並驗證物件路徑。                                                                                                                                                                                                                |
| [**Swbemobjectset 搭配使用**](swbemobjectset.md)             | 取得 [**SWbemObject**](swbemobject.md) 物件集合的存取權。                                                                                                                                                                             |
| [**SWbemPrivilege**](swbemprivilege.md)             | 設定或清除許可權。                                                                                                                                                                                                                            |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)       | 取得 [**SWbemPrivilege**](swbemprivilege.md) 物件集合的存取權。                                                                                                                                                                       |
| [**Swbempropertyset**](swbemproperty.md)               | 包含單一 WMI 屬性。                                                                                                                                                                                                                        |
| [**內含**](swbempropertyset.md)         | 取得 [**swbempropertyset**](swbemproperty.md) 物件集合的存取權。                                                                                                                                                                         |
| [**SWbemQualifier**](swbemqualifier.md)             | 包含單一屬性限定詞。                                                                                                                                                                                                                  |
| [**SWbemQualifierSet**](swbemqualifierset.md)       | 取得 [**SWbemQualifier**](swbemqualifier.md) 物件集合的存取權。                                                                                                                                                                       |
| [**SWbemRefresher**](swbemrefresher.md)             | 在一項作業中收集和更新物件屬性值。                                                                                                                                                                                          |
| [**SWbemRefreshableItem**](swbemrefreshableitem.md) | 代表 [**SWbemRefresher**](swbemrefresher.md) 物件中的單一可重新整理元素，例如屬性。                                                                                                                                     |
| [**SWbemSecurity**](swbemsecurity.md)               | 管理安全性設定，例如元件物件模型 (COM) [**許可權**](swbemsecurity-privileges.md)、 [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)和 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)。   |
| [**SWbemServices**](swbemservices.md)               | 建立、更新及抓取實例或類別。                                                                                                                                                                                                  |
| [**SWbemServicesEx**](swbemservicesex.md)           | 擴充 [**SWbemServices**](swbemservices.md)的功能。 這個物件會加入 [**Put**](swbemservicesex-put.md) 和 [**PutAsync**](swbemservicesex-putasync.md) 方法，以允許將類別或實例儲存至多個命名空間。 |
| [**SWbemSink**](swbemsink.md)                       | 接收用戶端應用程式所使用之非同步作業和事件通知的結果。                                                                                                                                        |



 

 

 



