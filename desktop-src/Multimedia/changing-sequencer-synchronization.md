---
title: 變更 Sequencer 同步處理
description: 變更 Sequencer 同步處理
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET 命令訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "106982121"
---
# <a name="changing-sequencer-synchronization"></a><span data-ttu-id="8a87f-104">變更 Sequencer 同步處理</span><span class="sxs-lookup"><span data-stu-id="8a87f-104">Changing Sequencer Synchronization</span></span>

> [!NOTE]
> <span data-ttu-id="8a87f-105">無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。</span><span class="sxs-lookup"><span data-stu-id="8a87f-105">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="8a87f-106">本檔中有 ' 從屬 ' 這個字的參考。</span><span class="sxs-lookup"><span data-stu-id="8a87f-106">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="8a87f-107">Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。</span><span class="sxs-lookup"><span data-stu-id="8a87f-107">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="8a87f-108">這種用語是用來做為軟體內所使用的用語。</span><span class="sxs-lookup"><span data-stu-id="8a87f-108">This wording is used as it is currently the wording used within the software.</span></span> <span data-ttu-id="8a87f-109">為求一致，本檔包含此字。</span><span class="sxs-lookup"><span data-stu-id="8a87f-109">For consistency, this document contains this word.</span></span> <span data-ttu-id="8a87f-110">從軟體移除此字組時，我們會將此檔修正為一致。</span><span class="sxs-lookup"><span data-stu-id="8a87f-110">When this word is removed from the software, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="8a87f-111">若要變更 sequencer 裝置的同步處理模式，請使用 [**mci \_ set**](mci-set.md) 命令訊息與 mci \_ SEQ \_ set \_ MASTER 和 mci \_ seq \_ set \_ 從屬旗標。</span><span class="sxs-lookup"><span data-stu-id="8a87f-111">To change the synchronization mode of a sequencer device, use the [**MCI\_SET**](mci-set.md) command message with the MCI\_SEQ\_SET\_MASTER and MCI\_SEQ\_SET\_SLAVE flags.</span></span> <span data-ttu-id="8a87f-112">[**MCI \_ SEQ \_ SET \_ PARMS**](mci-seq-set-parms.md) structure （ **dwMaster** 和 **dwSlave**）中的兩個成員是用來指定主要和次級同步處理模式。</span><span class="sxs-lookup"><span data-stu-id="8a87f-112">Two members in the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, **dwMaster** and **dwSlave**, are used to specify the master and subordinate synchronization modes.</span></span>

<span data-ttu-id="8a87f-113">主要同步處理模式會控制 sequencer 傳送至輸出埠的同步處理資訊。</span><span class="sxs-lookup"><span data-stu-id="8a87f-113">The master synchronization mode controls synchronization information sent by the sequencer to an output port.</span></span> <span data-ttu-id="8a87f-114">以下是 **dwMaster** 成員的常數及其對應的主要同步處理模式。</span><span class="sxs-lookup"><span data-stu-id="8a87f-114">Following are the constants for the **dwMaster** member and their corresponding master synchronization modes.</span></span>



| <span data-ttu-id="8a87f-115">常數</span><span class="sxs-lookup"><span data-stu-id="8a87f-115">Constant</span></span>        | <span data-ttu-id="8a87f-116">同步處理模式</span><span class="sxs-lookup"><span data-stu-id="8a87f-116">Synchronization mode</span></span>                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a87f-117">MCI \_ SEQ \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="8a87f-117">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="8a87f-118">MIDI 同步處理。</span><span class="sxs-lookup"><span data-stu-id="8a87f-118">MIDI Synchronization.</span></span> <span data-ttu-id="8a87f-119">使用 MIDI 計時時鐘訊息將計時資訊傳送至輸出埠。</span><span class="sxs-lookup"><span data-stu-id="8a87f-119">Send timing information to output port using MIDI timing clock messages.</span></span>   |
| <span data-ttu-id="8a87f-120">MCI \_ SEQ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="8a87f-120">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="8a87f-121">SMPTE 同步處理。</span><span class="sxs-lookup"><span data-stu-id="8a87f-121">SMPTE Synchronization.</span></span> <span data-ttu-id="8a87f-122">使用 MIDI 四分之一框架訊息將計時資訊傳送至輸出埠。</span><span class="sxs-lookup"><span data-stu-id="8a87f-122">Send timing information to output port using MIDI quarter-frame messages.</span></span> |
| <span data-ttu-id="8a87f-123">MCI \_ SEQ \_ 無</span><span class="sxs-lookup"><span data-stu-id="8a87f-123">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="8a87f-124">無同步處理。</span><span class="sxs-lookup"><span data-stu-id="8a87f-124">No Synchronization.</span></span> <span data-ttu-id="8a87f-125">不傳送任何時間資訊。</span><span class="sxs-lookup"><span data-stu-id="8a87f-125">Send no timing information.</span></span>                                                  |



 

<span data-ttu-id="8a87f-126">次級同步處理模式會控制 sequencer 取得其計時資訊以播放 MIDI 檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="8a87f-126">The subordinate synchronization mode controls where the sequencer gets its timing information to play a MIDI file.</span></span> <span data-ttu-id="8a87f-127">以下是 **dwSlave** 成員及其對應次級同步處理模式的常數。</span><span class="sxs-lookup"><span data-stu-id="8a87f-127">Following are the constants for the **dwSlave** member and their corresponding subordinate synchronization modes.</span></span>



| <span data-ttu-id="8a87f-128">常數</span><span class="sxs-lookup"><span data-stu-id="8a87f-128">Constant</span></span>        | <span data-ttu-id="8a87f-129">同步處理模式</span><span class="sxs-lookup"><span data-stu-id="8a87f-129">Synchronization mode</span></span>                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a87f-130">MCI \_ SEQ \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="8a87f-130">MCI\_SEQ\_FILE</span></span>  | <span data-ttu-id="8a87f-131">檔案同步處理。</span><span class="sxs-lookup"><span data-stu-id="8a87f-131">File Synchronization.</span></span> <span data-ttu-id="8a87f-132">從 MIDI 檔案取得計時資訊。</span><span class="sxs-lookup"><span data-stu-id="8a87f-132">Get timing information from MIDI file.</span></span>                                                                                       |
| <span data-ttu-id="8a87f-133">MCI \_ SEQ \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="8a87f-133">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="8a87f-134">MIDI 同步處理。</span><span class="sxs-lookup"><span data-stu-id="8a87f-134">MIDI Synchronization.</span></span> <span data-ttu-id="8a87f-135">使用 MIDI 計時時鐘訊息從輸入埠取得計時資訊。</span><span class="sxs-lookup"><span data-stu-id="8a87f-135">Get timing information from input port using MIDI timing clock messages.</span></span>                                                     |
| <span data-ttu-id="8a87f-136">MCI \_ SEQ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="8a87f-136">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="8a87f-137">SMPTE 同步處理。</span><span class="sxs-lookup"><span data-stu-id="8a87f-137">SMPTE Synchronization.</span></span> <span data-ttu-id="8a87f-138">使用 MIDI 四分之一框架訊息從輸入埠取得計時資訊。</span><span class="sxs-lookup"><span data-stu-id="8a87f-138">Get timing information from input port using MIDI quarter-frame messages.</span></span>                                                   |
| <span data-ttu-id="8a87f-139">MCI \_ SEQ \_ 無</span><span class="sxs-lookup"><span data-stu-id="8a87f-139">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="8a87f-140">無同步處理。</span><span class="sxs-lookup"><span data-stu-id="8a87f-140">No Synchronization.</span></span> <span data-ttu-id="8a87f-141">只取得來自 MCI 命令的計時資訊，並忽略時間資訊 (例如，MIDI 檔案中) 的節奏變更。</span><span class="sxs-lookup"><span data-stu-id="8a87f-141">Get timing information from MCI commands only and ignore timing information (such as tempo changes) that are in the MIDI file.</span></span> |



 

> [!Note]  
> <span data-ttu-id="8a87f-142">目前，在主要同步處理中，MCI MIDI sequencer 僅支援 (MCI \_ SEQ NONE) 的無同步處理模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8a87f-142">Currently, for master synchronization, the MCI MIDI sequencer supports only the No Synchronization mode (MCI\_SEQ\_NONE).</span></span> <span data-ttu-id="8a87f-143">針對次級同步處理，它只支援 (MCI seq 檔案的檔案同步處理模式， \_ \_) 和沒有任何同步處理模式 (MCI \_ seq \_ 無) 。</span><span class="sxs-lookup"><span data-stu-id="8a87f-143">For subordinate synchronization, it supports only the File Synchronization mode (MCI\_SEQ\_FILE) and the No Synchronization mode (MCI\_SEQ\_NONE).</span></span>

 

 

 




