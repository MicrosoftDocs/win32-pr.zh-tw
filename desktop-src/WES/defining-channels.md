---
title: 定義通道
description: 事件可以寫入事件記錄檔通道、事件追蹤記錄檔或兩者。 通道基本上是收集事件的接收。
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3c73697aa11e7b63ace0ece33be23ca7a1b883
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104092592"
---
# <a name="defining-channels"></a><span data-ttu-id="daa74-104">定義通道</span><span class="sxs-lookup"><span data-stu-id="daa74-104">Defining Channels</span></span>

<span data-ttu-id="daa74-105">事件可以寫入事件記錄檔通道、事件追蹤記錄檔或兩者。</span><span class="sxs-lookup"><span data-stu-id="daa74-105">Events can be written to event log channels, event tracing log files, or both.</span></span> <span data-ttu-id="daa74-106">通道基本上是收集事件的接收。</span><span class="sxs-lookup"><span data-stu-id="daa74-106">A channel is basically a sink that collects events.</span></span> <span data-ttu-id="daa74-107">如果您事件的目標物件使用事件取用者（例如 Windows 事件檢視器），則您必須定義新通道來收集您的事件，或匯入其他提供者所定義的現有通道。</span><span class="sxs-lookup"><span data-stu-id="daa74-107">If the target audience for your events uses event consumers such as the Windows Event Viewer, you must define new channels to collect your events or import an existing channel that another provider defined.</span></span>

<span data-ttu-id="daa74-108">若要定義您自己的通道，請使用 **通道** 元素。</span><span class="sxs-lookup"><span data-stu-id="daa74-108">To define your own channels, use the **channel** element.</span></span> <span data-ttu-id="daa74-109">若要定義匯入的通道，請使用 **importChannel** 元素。</span><span class="sxs-lookup"><span data-stu-id="daa74-109">To define an imported channel, use the **importChannel** element.</span></span> <span data-ttu-id="daa74-110">您可以在您定義的匯入通道或通道的任意組合中指定最多8個通道。</span><span class="sxs-lookup"><span data-stu-id="daa74-110">You can specify up to eight channels in any combination of imported channels or channels that you define.</span></span>

<span data-ttu-id="daa74-111">通道必須是下列四種類型之一：系統管理員、操作、分析和偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="daa74-111">The channel must be of one of four types: Admin, Operational, Analytic, and Debug.</span></span> <span data-ttu-id="daa74-112">每個通道類型都有一個目標物件，可決定您寫入通道的事件種類。</span><span class="sxs-lookup"><span data-stu-id="daa74-112">Each channel type has an intended audience, which determines the type of events that you write to the channel.</span></span> <span data-ttu-id="daa74-113">如需每種類型的說明，請參閱 [**ChannelType**](eventmanifestschema-channeltype-complextype.md) 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="daa74-113">For a description of each type, see the [**ChannelType**](eventmanifestschema-channeltype-complextype.md) complex type.</span></span>

<span data-ttu-id="daa74-114">若要指定要寫入事件的通道，請將事件定義的 **通道** 屬性設定為與通道定義之 **子** 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="daa74-114">To specify the channel to which an event is written, set the event definition's **channel** attribute to the same value as the channel definition's **chid** attribute.</span></span> <span data-ttu-id="daa74-115">事件一次只能寫入一個通道，但也可同時由多達7個其他 ETW 會話收集。</span><span class="sxs-lookup"><span data-stu-id="daa74-115">Events can only be written to one channel at a time, but can also be collected by up to 7 other ETW sessions at the same time.</span></span>

<span data-ttu-id="daa74-116">下列範例顯示如何匯入通道。</span><span class="sxs-lookup"><span data-stu-id="daa74-116">The following example shows how to import a channel.</span></span> <span data-ttu-id="daa74-117">您必須設定 **子** 和 **name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="daa74-117">You must set the **chid** and **name** attributes.</span></span> <span data-ttu-id="daa74-118">**子** 屬性可唯一識別通道，通道清單中的每個通道識別碼都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="daa74-118">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="daa74-119">將 [ **名稱** ] 屬性設定為提供者在定義通道時所用的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="daa74-119">Set the **name** attribute to the same name that the provider used when it defined the channel.</span></span>


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

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

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

<span data-ttu-id="daa74-120">雖然 Winmeta.xml 定義您可以匯入的舊版通道，但除非您支援取用舊版通道以外的取用者，否則您不應該使用這些通道 (例如，應用程式或系統) 。</span><span class="sxs-lookup"><span data-stu-id="daa74-120">Although Winmeta.xml defines legacy channels that you can import, you should not use them unless you are supporting legacy consumers that consume events out of the legacy channels (for example, Application or System).</span></span> <span data-ttu-id="daa74-121">Winmeta.xml 檔案包含在 Windows SDK 中。</span><span class="sxs-lookup"><span data-stu-id="daa74-121">The Winmeta.xml file is included in the Windows SDK.</span></span>

<span data-ttu-id="daa74-122">下列範例顯示如何定義通道。</span><span class="sxs-lookup"><span data-stu-id="daa74-122">The following example shows how to define a channel.</span></span> <span data-ttu-id="daa74-123">您必須設定 [ **子**]、[ **名稱**] 和 [ **類型** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="daa74-123">You must set the **chid**, **name**, and **type** attributes.</span></span> <span data-ttu-id="daa74-124">**子** 屬性可唯一識別通道，通道清單中的每個通道識別碼都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="daa74-124">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="daa74-125">將 **子** 屬性設定為提供者所列出通道的唯一值;通道識別碼是在您的一或多個事件定義中參考。</span><span class="sxs-lookup"><span data-stu-id="daa74-125">Set the **chid** attribute to a value that is unique for the channels that your provider lists; the channel identifier is referenced in one or more of your event definitions.</span></span> <span data-ttu-id="daa74-126">命名通道的慣例是在表單中使用提供者名稱和通道類型（ *providername* / *channeltype*）。</span><span class="sxs-lookup"><span data-stu-id="daa74-126">The convention for naming the channel is to use the provider name and channel type in the form, *providername*/*channeltype*.</span></span>

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

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
