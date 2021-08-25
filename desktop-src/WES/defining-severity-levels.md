---
title: 定義嚴重性層級
description: 層級可用來將事件分組，通常表示事件的嚴重性或詳細程度。
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3c3c5e663e476f98bef5c9be3f20cae5e0e88a74a7996f6f515d1d92599eb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863678"
---
# <a name="defining-severity-levels"></a>定義嚴重性層級

層級可用來將事件分組，通常表示事件的嚴重性或詳細程度。 若要定義層級，請使用 **level** 元素。 Winmeta.xml 檔案會定義下列常用的嚴重性層級：

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

取用者會使用層級來查詢包含特定層級值的事件。 ETW 追蹤會話也可以使用層級來限制寫入事件追蹤記錄檔的事件;層級值等於或小於指定層級值的事件會寫入記錄檔中。 例如，如果會話指定了 win： Warning 的層級值，記錄檔就會包含警告、錯誤和重大事件。

下列範例顯示如何定義層級。 您必須指定層級的 **名稱** 和 **值** 屬性。 **Value** 屬性的值必須在16到255的範圍內。 **符號** 和 **訊息** 屬性是選擇性的。


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

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
