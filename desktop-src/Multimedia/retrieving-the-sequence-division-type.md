---
title: 正在抓取序列除法類型
description: 正在抓取序列除法類型
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- 音樂檢測數位介面 (MIDI) ，序列除法類型
- MIDI (音樂檢測數位介面) ，序列除法類型
- MCI MIDI sequencer，除法類型
- MCI_STATUS 命令
- sequence 除法類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932164"
---
# <a name="retrieving-the-sequence-division-type"></a><span data-ttu-id="c7d66-108">正在抓取序列除法類型</span><span class="sxs-lookup"><span data-stu-id="c7d66-108">Retrieving the Sequence Division Type</span></span>

<span data-ttu-id="c7d66-109">MIDI 順序的 *部門型* 別決定了序列中的 MIDI 事件之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="c7d66-109">The *division type* of a MIDI sequence determines the amount of time between MIDI events in the sequence.</span></span> <span data-ttu-id="c7d66-110">若要判斷序列的除法類型，請使用 [**mci \_ status**](mci-status.md)命令，並將 [**mci \_ status \_ PARMS**](mci-status-parms.md)結構的 **dwItem** 成員設定為 mci \_ SEQ \_ status \_ DIVTYPE。</span><span class="sxs-lookup"><span data-stu-id="c7d66-110">To determine the division type of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_DIVTYPE .</span></span>

<span data-ttu-id="c7d66-111">如果 **mci \_ status** 命令成功， **mci \_ status \_ PARMS** 結構的 **dwReturn** 成員會包含下列其中一個值，以指出除法類型。</span><span class="sxs-lookup"><span data-stu-id="c7d66-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure will contain one of the following values to indicate the division type.</span></span>



| <span data-ttu-id="c7d66-112">值</span><span class="sxs-lookup"><span data-stu-id="c7d66-112">Value</span></span>                        | <span data-ttu-id="c7d66-113">除法類型</span><span class="sxs-lookup"><span data-stu-id="c7d66-113">Division type</span></span>                     |
|------------------------------|-----------------------------------|
| <span data-ttu-id="c7d66-114">MCI \_ SEQ \_ DIV \_ PPQN</span><span class="sxs-lookup"><span data-stu-id="c7d66-114">MCI\_SEQ\_DIV\_PPQN</span></span>          | <span data-ttu-id="c7d66-115">PPQN (部分-每季附注) </span><span class="sxs-lookup"><span data-stu-id="c7d66-115">PPQN (parts-per-quarter note)</span></span>     |
| <span data-ttu-id="c7d66-116">MCI \_ SEQ \_ DIV （ \_ SMPTE \_ 24）</span><span class="sxs-lookup"><span data-stu-id="c7d66-116">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>     | <span data-ttu-id="c7d66-117">SMPTE，每秒 24 fps (畫面) </span><span class="sxs-lookup"><span data-stu-id="c7d66-117">SMPTE, 24 fps (frames per second)</span></span> |
| <span data-ttu-id="c7d66-118">MCI \_ SEQ \_ DIV 的 \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="c7d66-118">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>     | <span data-ttu-id="c7d66-119">SMPTE，25 fps</span><span class="sxs-lookup"><span data-stu-id="c7d66-119">SMPTE, 25 fps</span></span>                     |
| <span data-ttu-id="c7d66-120">MCI \_ SEQ \_ DIV \_ \_ 30</span><span class="sxs-lookup"><span data-stu-id="c7d66-120">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>     | <span data-ttu-id="c7d66-121">SMPTE，30 fps</span><span class="sxs-lookup"><span data-stu-id="c7d66-121">SMPTE, 30 fps</span></span>                     |
| <span data-ttu-id="c7d66-122">MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="c7d66-122">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span> | <span data-ttu-id="c7d66-123">SMPTE，30 fps 捨棄框架</span><span class="sxs-lookup"><span data-stu-id="c7d66-123">SMPTE, 30 fps drop frame</span></span>          |



 

<span data-ttu-id="c7d66-124">您必須知道順序的除法類型才能變更或查詢其節奏。</span><span class="sxs-lookup"><span data-stu-id="c7d66-124">You must know the division type of a sequence to change or query its tempo.</span></span> <span data-ttu-id="c7d66-125">您無法使用 MCI sequencer 來變更序列的除法類型。</span><span class="sxs-lookup"><span data-stu-id="c7d66-125">You cannot change the division type of a sequence by using the MCI sequencer.</span></span>

 

 




