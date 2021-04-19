---
description: 為 C/c + + 程式設計人員提供適用于 WMI 的腳本 API 的介面，以取代 COM API 版本。
ms.assetid: 18f6cc70-9df1-4d43-a2e0-af03e2f9e2c5
ms.tgt_platform: multiple
title: 自動化介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652e9a1fb35a66bddb9f0aebe543770e89e6e2ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985052"
---
# <a name="automation-interfaces"></a>自動化介面

自動化 API 可讓 C/c + + 程式設計人員使用適用于 WMI 的腳本 API 的介面，取代 COM API 的版本。

下表列出 WMI 物件，以及如何在自動化 API 中使用它們。 適用于 WMI 對等的腳本 API 之介面檔的交互參照連結。



| Automation 物件                                 | Description                                                                                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**ISWbemEventSource**](swbemeventsource.md)     | 與 [**ISWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)一起抓取事件。   |
| [**ISWbemLastError**](swbemlasterror.md)         | 當發生錯誤時，提供延伸的錯誤資訊。                                                                   |
| [**ISWbemLocator**](swbemlocator.md)             | 取得 [**ISWbemServices**](swbemservices.md) 物件的參考，該物件可以存取特定主機電腦上的 WMI。 |
| [**ISWbemMethod**](swbemmethod.md)               | 包含單一方法定義。                                                                                        |
| [**ISWbemMethodSet**](swbemmethodset.md)         | 取得 [**ISWbemMethod**](swbemmethod.md) 物件集合的存取權。                                                 |
| [**ISWbemNamedValue**](swbemnamedvalue.md)       | 包含單一的名稱值。                                                                                              |
| [**ISWbemNamedValueSet**](swbemnamedvalueset.md) | 取得 [**ISWbemNamedValue**](swbemnamedvalue.md) 物件集合的存取權。                                         |
| [**ISWbemObject**](swbemobject.md)               | 包含和操作單一通用訊息模型 (CIM) 物件類別或實例。                                  |
| [**ISWbemObjectPath**](swbemobjectpath.md)       | 產生並驗證物件路徑。                                                                                     |
| [**ISWbemObjectSet**](swbemobjectset.md)         | 取得 [**ISWbemObject**](swbemobject.md) 物件集合的存取權。                                                 |
| [**ISWbemPrivilege**](swbemprivilege.md)         | 設定或清除許可權。                                                                                                 |
| [**ISWbemPrivilegeSet**](swbemprivilegeset.md)   | 取得 [**ISWbemPrivilege**](swbemprivilege.md) 物件集合的存取權。                                           |
| [**ISWbemProperty**](swbemproperty.md)           | 用來包含單一 CIM 屬性。                                                                                      |
| [**ISWbemPropertySet**](swbempropertyset.md)     | 取得 [**ISWbemProperty**](swbemproperty.md) 物件集合的存取權。                                              |
| [**ISWbemQualifier**](swbemqualifier.md)         | 包含單一類別限定詞。                                                                                          |
| [**ISWbemQualifierSet**](swbemqualifierset.md)   | 取得 [**ISWbemQualifier**](swbemqualifier.md) 物件集合的存取權。                                           |
| [**ISWbemSecurity**](swbemsecurity.md)           | 管理安全性設定，例如元件物件模型 (COM) 許可權、AuthenticationLevel 和 ImpersonationLevel。      |
| [**ISWbemServices**](swbemservices.md)           | 建立、更新及抓取實例或類別。                                                                       |
| [**ISWbemSink**](swbemsink.md)                   | 接收用戶端應用程式非同步作業和事件通知的結果。                                 |



 

 

 



