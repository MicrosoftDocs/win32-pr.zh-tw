---
description: 描述讀取 WMI 腳本 API 主題的檔慣例。
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: 腳本 API 的檔慣例
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319672"
---
# <a name="document-conventions-for-the-scripting-api"></a>腳本 API 的檔慣例

[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)參考會使用下列檔慣例：

-   參數類型的定義是使用前置詞： b (布林值) 、str (字串) 、I (整數) 、obj (Automation 物件) 、var (變異) 。
-   選擇性參數會以方括弧括住，並以指派顯示其預設值。
-   在物件參數的情況下，"obj" 前置詞後面的字元會指出所需的物件類型。



| 物件參數      | 物件型別                                          |
|-----------------------|------------------------------------------------------|
| *WbemDatetime*        | [**SWbemDateTime**](swbemdatetime.md)               |
| *WbemEventSource*     | [**SWbemEventSource**](swbemeventsource.md)         |
| *WbemLocator*         | [**Wbemscripting.swbemlocator**](swbemlocator.md)                 |
| *WbemMethod*          | [**SWbemMethod**](swbemmethod.md)                   |
| *WbemMethodSet*       | [**SWbemMethodSet**](swbemmethodset.md)             |
| *WbemNamedValueSet*   | [**SWbemNamedValueSet**](swbemnamedvalueset.md)     |
| *WbemObject*          | [**SWbemObject**](swbemobject.md)                   |
| *WbemObjectEx*        | [**SWbemObjectEx**](swbemobjectex.md)               |
| *WbemObjectPath*      | [**SWbemObjectPath**](swbemobjectpath.md)           |
| *WbemObjectSet*       | [**Swbemobjectset 搭配使用**](swbemobjectset.md)             |
| *WbemPrivilege*       | [**SWbemPrivilege**](swbemprivilege.md)             |
| *WbemPrivilegeSet*    | [**SWbemPrivilegeSet**](swbemprivilegeset.md)       |
| *WbemProperty*        | [**Swbempropertyset**](swbemproperty.md)               |
| *WbemPropertySet*     | [**內含**](swbempropertyset.md)         |
| *WbemQualifier*       | [**SWbemQualifier**](swbemqualifier.md)             |
| *WbemQualifierSet*    | [**SWbemQualifierSet**](swbemqualifierset.md)       |
| *WbemRefreshableItem* | [**SWbemRefreshableItem**](swbemrefreshableitem.md) |
| *WbemRefresher*       | [**SWbemRefresher**](swbemrefresher.md)             |
| *WbemServices*        | [**SWbemServices**](swbemservices.md)               |
| *WbemServicesEx*      | [**SWbemServicesEx**](swbemservicesex.md)           |



 

例如，下列程式碼會示範如何為不同類型的物件命名變數：


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



