---
title: 識別提供者
description: 資訊清單可以識別一或多個提供者。 若要識別提供者，請使用 provider 元素。
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45941a540f8804beccc408435fc202593ddad601
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104507840"
---
# <a name="identifying-the-provider"></a>識別提供者

資訊清單可以識別一或多個提供者。 若要識別提供者，請使用 **provider** 元素。 您必須指定 **name**、 **guid**、 **resourceFileName**、 **messageFileName** 和 **symbol** 屬性。 如果您將資訊清單當地語系化，您也應該指定 **訊息** 屬性，取用者會使用此屬性來顯示提供者的名稱。 如果您未指定 **訊息** 屬性，取用者會使用 **name** 屬性的值。

您最多可以在資訊清單中識別16個提供者。 如果您想要識別16個以上的提供者，則必須包含資訊清單的 **messageTable** 區段，第十七個和 on 提供者必須使用此區段來指派其定義之訊息字串的資源值，訊息資料表不能包含提供者1到16的任何訊息字串。

下列範例示範如何使用 **provider** 元素來識別提供者。


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
