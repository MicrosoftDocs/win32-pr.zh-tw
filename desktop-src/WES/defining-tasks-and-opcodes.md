---
title: 定義工作和作業碼
description: 提供者會使用工作和操作碼以邏輯方式分組事件。 群組事件可協助取用者只查詢包含特定工作和作業碼組合的事件。
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb576251edf4de14c564c6e468209ece93e5840da9e0d821c20b132794f48ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032468"
---
# <a name="defining-tasks-and-opcodes"></a>定義工作和作業碼

提供者會使用工作和操作碼以邏輯方式分組事件。 群組事件可協助取用者只查詢包含特定工作和作業碼組合的事件。 一般而言，您會使用工作來識別提供者的主要元件，例如網路或資料庫元件。 然後，您可以使用操作碼來識別元件執行的作業，例如網路元件的傳送和接收作業。 如果您只有一個元件，則可以使用 [工作] 反映元件中的主要作業，例如 [連接] 或 [中斷連接]，然後使用 opcode 來反映作業內的活動，例如讀取登錄。 您也可以在不指定工作的情況下使用操作碼。 您可以使用工作和操作碼來分組取用者的事件，完全由您決定。

若要定義工作，請使用 **task** 元素。 若要定義作業碼，請使用 **opcode** 元素。 您最多可以指定228碼。 工作 **值** 必須大於0。 Opcode 的範圍必須在11到239之間。 Winmeta.xml 的檔案會定義您可以使用的一般作業，而不是定義您自己的作業。

下列範例將示範如何定義數個工作和操作碼。

```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <tasks>
                    <task name="Disconnect" 
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>
 
                    <task name="Connect" 
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)">
                    </task>

                    <task name="Validate" 
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)">
                    </task>
                </tasks>

                <opcodes>
                    <opcode name="Initialize" 
                            symbol="OPCODE_INITIALIZE" 
                            value="12"
                            message="$(string.Opcode.Initialize)"/>

                    <opcode name="Cleanup" 
                            symbol="OPCODE_CLEANUP" 
                            value="13"
                            message="$(string.Opcode.Cleanup)"/>
                 </opcodes>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
