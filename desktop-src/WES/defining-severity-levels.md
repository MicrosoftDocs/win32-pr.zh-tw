---
title: 定義嚴重性層級
description: 層級可用來將事件分組，通常表示事件的嚴重性或詳細程度。
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104374868"
---
# <a name="defining-severity-levels"></a><span data-ttu-id="6f6dc-103">定義嚴重性層級</span><span class="sxs-lookup"><span data-stu-id="6f6dc-103">Defining Severity Levels</span></span>

<span data-ttu-id="6f6dc-104">層級可用來將事件分組，通常表示事件的嚴重性或詳細程度。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-104">Levels are used to group events and typically indicate the severity or verbosity of an event.</span></span> <span data-ttu-id="6f6dc-105">若要定義層級，請使用 **level** 元素。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-105">To define a level, use the **level** element.</span></span> <span data-ttu-id="6f6dc-106">Winmeta.xml 檔案會定義下列常用的嚴重性層級：</span><span class="sxs-lookup"><span data-stu-id="6f6dc-106">The Winmeta.xml file defines the following commonly used severity levels:</span></span>

-   <span data-ttu-id="6f6dc-107">win:Critical</span><span class="sxs-lookup"><span data-stu-id="6f6dc-107">win:Critical</span></span>
-   <span data-ttu-id="6f6dc-108">win:Error</span><span class="sxs-lookup"><span data-stu-id="6f6dc-108">win:Error</span></span>
-   <span data-ttu-id="6f6dc-109">win:Warning</span><span class="sxs-lookup"><span data-stu-id="6f6dc-109">win:Warning</span></span>
-   <span data-ttu-id="6f6dc-110">win:Informational</span><span class="sxs-lookup"><span data-stu-id="6f6dc-110">win:Informational</span></span>
-   <span data-ttu-id="6f6dc-111">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="6f6dc-111">win:Verbose</span></span>

<span data-ttu-id="6f6dc-112">取用者會使用層級來查詢包含特定層級值的事件。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-112">Consumers use levels to query for events that contain a specific level value.</span></span> <span data-ttu-id="6f6dc-113">ETW 追蹤會話也可以使用層級來限制寫入事件追蹤記錄檔的事件;層級值等於或小於指定層級值的事件會寫入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-113">An ETW tracing session can also use levels to limit the events that are written to the event tracing log file; events with a level value equal to or less than the specified level value are written to the log file.</span></span> <span data-ttu-id="6f6dc-114">例如，如果會話指定了 win： Warning 的層級值，記錄檔就會包含警告、錯誤和重大事件。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-114">For example, if the session specified the level value for win:Warning, the log file would contain warning, error, and critical events.</span></span>

<span data-ttu-id="6f6dc-115">下列範例顯示如何定義層級。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-115">The following example shows how to define a level.</span></span> <span data-ttu-id="6f6dc-116">您必須指定層級的 **名稱** 和 **值** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-116">You must specify the level's **name** and **value** attributes.</span></span> <span data-ttu-id="6f6dc-117">**Value** 屬性的值必須在16到255的範圍內。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-117">The value of the **value** attribute must be in the range from 16 through 255.</span></span> <span data-ttu-id="6f6dc-118">**符號** 和 **訊息** 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6f6dc-118">The **symbol** and **message** attributes are optional.</span></span>


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
