---
title: 定義篩選器
description: 提供者可以定義篩選器，讓會話用來根據事件資料篩選事件。
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093167"
---
# <a name="defining-filters"></a><span data-ttu-id="2a566-103">定義篩選器</span><span class="sxs-lookup"><span data-stu-id="2a566-103">Defining Filters</span></span>

<span data-ttu-id="2a566-104">提供者可以定義篩選器，讓會話用來根據事件資料篩選事件。</span><span class="sxs-lookup"><span data-stu-id="2a566-104">A provider can define filters that a session uses to filter events based on event data.</span></span> <span data-ttu-id="2a566-105">使用 level 和關鍵字時，ETW 會判斷是否將事件寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2a566-105">With level and keywords, ETW determines whether the event is written to the log.</span></span> <span data-ttu-id="2a566-106">不過，使用篩選準則時，提供者會使用控制會話傳遞給它的篩選資料準則 (請參閱 [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) 函式) ，判斷它是否會將事件寫入該會話。</span><span class="sxs-lookup"><span data-stu-id="2a566-106">However, with filters, the provider uses the filter data criteria that the controlling session passes to it (see the [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) function) to determine whether it writes the event to that session.</span></span> <span data-ttu-id="2a566-107">只有當 ETW 追蹤會話啟用您的提供者時，篩選才適用。</span><span class="sxs-lookup"><span data-stu-id="2a566-107">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="2a566-108">一般而言，提供者只會寫入事件，而會話會識別它想要使用層級和關鍵字的事件種類。</span><span class="sxs-lookup"><span data-stu-id="2a566-108">Typically, providers just write events, and the session identifies the types of events that it wants using level and keywords.</span></span> <span data-ttu-id="2a566-109">如果提供者已定義事件種類的資料篩選，則會話可以使用它來根據事件資料篩選出該事件種類的事件， (由提供者) 定義篩選準則的語法。</span><span class="sxs-lookup"><span data-stu-id="2a566-109">If the provider defined a data filter for an event type, the session could use it to filter out events for that event type based on the event data (the semantics of the filter is defined by the provider).</span></span> <span data-ttu-id="2a566-110">例如，如果您的提供者會產生處理事件，則您可以定義篩選以進程識別碼為基礎的處理事件的資料篩選。</span><span class="sxs-lookup"><span data-stu-id="2a566-110">For example, if your provider generates process events, you could define a data filter that filtered process events based on a process identifier.</span></span> <span data-ttu-id="2a566-111">然後，會話可以將處理序識別碼做為篩選資料傳遞給提供者，並只接收該處理常式識別碼的處理事件。</span><span class="sxs-lookup"><span data-stu-id="2a566-111">The session could then pass a process identifier as filter data to the provider and receive only process events for that process identifier.</span></span>

<span data-ttu-id="2a566-112">下列範例示範如何使用 **filter** 元素來定義篩選準則。</span><span class="sxs-lookup"><span data-stu-id="2a566-112">The following example shows how to use the **filter** element to define a filter.</span></span> <span data-ttu-id="2a566-113">您必須指定篩選的 **名稱** 和 **值** 屬性;其他屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2a566-113">You must specify the filter's **name** and **value** attributes; the other attributes are optional.</span></span> <span data-ttu-id="2a566-114">如果篩選準則需要會話通過篩選資料，則需要有 **tid** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2a566-114">The **tid** attribute is required if the filter requires that the session pass filter data.</span></span>


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

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```