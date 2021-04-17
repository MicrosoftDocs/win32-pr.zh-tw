---
title: 查詢 MIDI 裝置
description: 查詢 MIDI 裝置
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- " (MIDI) 的音樂檢測數位介面，查詢裝置"
- MIDI (的音樂檢測數位介面) ，查詢裝置
- MIDI 服務，查詢裝置
- 查詢 MIDI 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375048"
---
# <a name="querying-midi-devices"></a><span data-ttu-id="83c2a-107">查詢 MIDI 裝置</span><span class="sxs-lookup"><span data-stu-id="83c2a-107">Querying MIDI Devices</span></span>

<span data-ttu-id="83c2a-108">在播放或錄製 MIDI 資料之前，您必須先判斷出系統中的 MIDI 硬體有哪些功能。</span><span class="sxs-lookup"><span data-stu-id="83c2a-108">Before playing or recording MIDI data, you must determine the capabilities of the MIDI hardware present in the system.</span></span> <span data-ttu-id="83c2a-109">MIDI 功能可能會因一部多媒體電腦而異;應用程式不應對指定系統中的硬體提出假設。</span><span class="sxs-lookup"><span data-stu-id="83c2a-109">MIDI capability can vary from one multimedia computer to the next; applications should not make assumptions about the hardware present in a given system.</span></span>

<span data-ttu-id="83c2a-110">Windows 提供下列功能，以判斷指定系統中有多少部 MIDI 裝置可供輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="83c2a-110">Windows provides the following functions to determine how many MIDI devices are available for input or output in a given system.</span></span>



| <span data-ttu-id="83c2a-111">值</span><span class="sxs-lookup"><span data-stu-id="83c2a-111">Value</span></span>                                          | <span data-ttu-id="83c2a-112">意義</span><span class="sxs-lookup"><span data-stu-id="83c2a-112">Meaning</span></span>                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="83c2a-113">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="83c2a-113">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | <span data-ttu-id="83c2a-114">抓取系統中出現的 MIDI 輸入裝置數目。</span><span class="sxs-lookup"><span data-stu-id="83c2a-114">Retrieves the number of MIDI input devices present in the system.</span></span>  |
| [<span data-ttu-id="83c2a-115">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="83c2a-115">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | <span data-ttu-id="83c2a-116">抓取系統中出現的 MIDI 輸出裝置數目。</span><span class="sxs-lookup"><span data-stu-id="83c2a-116">Retrieves the number of MIDI output devices present in the system.</span></span> |



 

<span data-ttu-id="83c2a-117">就像其他音訊裝置一樣，MIDI 裝置是由裝置識別碼來識別，而這是由指定系統中的裝置數目隱含決定。</span><span class="sxs-lookup"><span data-stu-id="83c2a-117">Like other audio devices, MIDI devices are identified by a device identifier, which is determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="83c2a-118">裝置識別碼的範圍從零到已存在的裝置數目，減去一。</span><span class="sxs-lookup"><span data-stu-id="83c2a-118">Device identifiers range from zero to the number of devices present, minus one.</span></span> <span data-ttu-id="83c2a-119">例如，如果系統中有兩個 MIDI 輸出裝置，則有效的裝置識別碼為0和1。</span><span class="sxs-lookup"><span data-stu-id="83c2a-119">For example, if there are two MIDI output devices in a system, valid device identifiers are 0 and 1.</span></span>

<span data-ttu-id="83c2a-120">判斷出系統中有多少個 MIDI 輸入或輸出裝置之後，您就可以查詢每個裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="83c2a-120">After you determine how many MIDI input or output devices are present in a system, you can inquire about the capabilities of each device.</span></span> <span data-ttu-id="83c2a-121">Windows 提供下列功能來判斷音訊裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="83c2a-121">Windows provides the following functions to determine the capabilities of audio devices.</span></span>



| <span data-ttu-id="83c2a-122">值</span><span class="sxs-lookup"><span data-stu-id="83c2a-122">Value</span></span>                                          | <span data-ttu-id="83c2a-123">意義</span><span class="sxs-lookup"><span data-stu-id="83c2a-123">Meaning</span></span>                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83c2a-124">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="83c2a-124">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | <span data-ttu-id="83c2a-125">抓取指定之 MIDI 輸入裝置的功能，並將這項資訊放在 [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) 結構中。</span><span class="sxs-lookup"><span data-stu-id="83c2a-125">Retrieves the capabilities of a given MIDI input device and places this information in the [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure.</span></span>    |
| [<span data-ttu-id="83c2a-126">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="83c2a-126">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | <span data-ttu-id="83c2a-127">抓取指定之 MIDI 輸出裝置的功能，並將這項資訊放在 [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) 結構中。</span><span class="sxs-lookup"><span data-stu-id="83c2a-127">Retrieves the capabilities of a given MIDI output device and places this information in the [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) structure.</span></span> |



 

<span data-ttu-id="83c2a-128">這些函式中的每一個都有參數，可指定函式所填滿的結構位址，以及指定裝置功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83c2a-128">Each of these functions has a parameter specifying the address of a structure that the function fills with information about the capabilities of a specified device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83c2a-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="83c2a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83c2a-130">MIDI 服務</span><span class="sxs-lookup"><span data-stu-id="83c2a-130">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 