---
title: 定義用來分類事件種類的關鍵字
description: 提供者會使用關鍵字來分類不同類型的事件。
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "103841979"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a><span data-ttu-id="34114-103">定義用來分類事件種類的關鍵字</span><span class="sxs-lookup"><span data-stu-id="34114-103">Defining Keywords Used to Classify Types of Events</span></span>

<span data-ttu-id="34114-104">提供者會使用關鍵字來分類不同類型的事件。</span><span class="sxs-lookup"><span data-stu-id="34114-104">Providers use keywords to classify different types of events.</span></span> <span data-ttu-id="34114-105">例如，您可以建立所有讀取事件的關鍵字，然後將 read 關鍵字套用至任何執行讀取作業的事件，例如從檔案或登錄讀取。</span><span class="sxs-lookup"><span data-stu-id="34114-105">For example, you can create a keyword for all read events and then apply the read keyword to any event that performs a read operation such as reading from a file or registry.</span></span> <span data-ttu-id="34114-106">接著，取用者可以使用關鍵字位值來篩選不同的事件分類。</span><span class="sxs-lookup"><span data-stu-id="34114-106">Consumers could then use the keyword bit values to filter for different classification of events.</span></span> <span data-ttu-id="34114-107">例如，如果您也要依工作) 將事件分組，取用者可以要求工作 X (中的所有讀取事件或所有讀取事件。</span><span class="sxs-lookup"><span data-stu-id="34114-107">For example, the consumer could request all read events or all read events from task X (if you also group events by task).</span></span> <span data-ttu-id="34114-108">若要定義關鍵字，請使用 **關鍵字** 元素。</span><span class="sxs-lookup"><span data-stu-id="34114-108">To define a keyword, use the **keyword** element.</span></span>

<span data-ttu-id="34114-109">ETW 追蹤會話可以使用關鍵字 (其使用層級) 來限制 ETW 服務寫入事件追蹤記錄檔的事件。</span><span class="sxs-lookup"><span data-stu-id="34114-109">An ETW tracing session can use the keywords (in the same way that it uses level) to limit the events that the ETW service writes to its event tracing log file.</span></span> <span data-ttu-id="34114-110">追蹤會話可以使用兩組關鍵字位元遮罩來啟用提供者：如果任何事件的關鍵字位符合在此遮罩中設定的任何位，則為事件寫入的「任何」位元遮罩，以及符合「任何」案例之事件的「全部」位元遮罩，則只有在事件的關鍵字位中有 "All" 遮罩中的所有位時，才會寫入事件。</span><span class="sxs-lookup"><span data-stu-id="34114-110">A tracing session can enable the provider using two sets of keyword bitmasks: an "Any" bitmask where the event is written if any of the event's keyword bits match any of the bits set in this mask, and an "All" bitmask where for those events that matched the "Any" case, the event is written only if all of the bits in the "All" mask exist in the event's keyword bitmask.</span></span>

<span data-ttu-id="34114-111">例如，如果提供者定義的事件指定 read 關鍵字 (位 0) 和本機存取關鍵字 (位 1) ，另外還有第二個事件，可指定讀取關鍵字 (位 0) 和遠端存取關鍵字 (位 2) ，您可以將 "Any" 位元遮罩設為1以接收所有讀取事件，或是將 "Any" 位元遮罩設為1，並將 "All" 位元遮罩設定為3，以只接收本機讀取。</span><span class="sxs-lookup"><span data-stu-id="34114-111">For example, if the provider defines an event that specifies a read keyword (bit 0) and a local access keyword (bit 1), and a second event that specifies a read keyword (bit 0) and a remote access keyword (bit 2), you could set the "Any" bitmask to 1 to receive all read events, or you could set the "Any" bitmask to 1 and "All" bitmask to 3 to receive only local reads.</span></span>

<span data-ttu-id="34114-112">您必須指定關鍵字的 **名稱** 和 **遮罩** 屬性。</span><span class="sxs-lookup"><span data-stu-id="34114-112">You must specify the keyword's **name** and **mask** attributes.</span></span> <span data-ttu-id="34114-113">遮罩只能設定一個位，介於 bit 0 和 bit 47 之間。</span><span class="sxs-lookup"><span data-stu-id="34114-113">The mask must set only one bit, between bit 0 and bit 47.</span></span> <span data-ttu-id="34114-114">保留的位48到64。</span><span class="sxs-lookup"><span data-stu-id="34114-114">Bits 48 through 64 are reserved.</span></span>

<span data-ttu-id="34114-115">**符號** 和 **訊息** 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="34114-115">The **symbol** and **message** attributes are optional.</span></span>

<span data-ttu-id="34114-116">下列範例顯示如何定義關鍵字。</span><span class="sxs-lookup"><span data-stu-id="34114-116">The following example shows how to define a keyword.</span></span>

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

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
