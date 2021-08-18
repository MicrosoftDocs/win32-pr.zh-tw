---
description: 您可以藉由連接到 wmi，然後呼叫 CreateObject，在 Visual Basic 腳本版本 (VBScript) 中建立 WMI 的物件。 下表列出支持對象建立之 WMI 的腳本 API 中的方法。
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: 使用 VBScript 建立物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e86dbc649d5feab471485dbdf536cde911c139aeab3b6eb3323b24199438d1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244568"
---
# <a name="creating-an-object-using-vbscript"></a>使用 VBScript 建立物件

您可以藉由連接到 wmi，然後呼叫[CreateObject](/previous-versions//xzysf6hc(v=vs.85))，在 Visual Basic 腳本版本 (VBScript) 中建立 WMI 的物件。 下表列出支持對象建立之 WMI 的腳本 API 中的方法。



| 介面                                        | ProgID                             |
|--------------------------------------------------|------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)           | "WbemScripting.SwbemDateTime"      |
| [**Wbemscripting.swbemlocator**](swbemlocator.md)             | "WbemScripting. Wbemscripting.swbemlocator"       |
| [**SWbemLastError**](swbemlasterror.md)         | "WbemScripting. SWbem. LastError"    |
| [**SWbemObjectPath**](swbemobjectpath.md)       | "WbemScripting.SWbemObjectPath"    |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | "WbemScripting.SWbemNamedValueSet" |
| [**SWbemRefresher**](swbemrefresher.md)         | "WbemScripting.SWbemRefresher"     |
| [**SWbemSink**](swbemsink.md)                   | "WbemScripting. SWbemSink"          |



 

下列程式描述如何使用 VBScript 建立 WMI 物件。

**使用 VBScript 建立 WMI 物件**

1.  使用名字或 [**wbemscripting.swbemlocator**](swbemlocator.md)物件連線至 WMI。

    如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。

2.  對 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 方法進行呼叫。

    下列程式碼範例顯示如何建立物件。

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    如果您在步驟1中使用了標記，就不需要再次呼叫 [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 。

 

 
