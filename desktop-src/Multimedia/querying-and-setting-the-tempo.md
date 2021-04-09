---
title: 查詢及設定節奏
description: 查詢及設定節奏
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- " (MIDI) 的音樂檢測數位介面，節奏"
- MIDI (的音樂檢測數位介面) 、節奏
- MCI MIDI sequencer，節奏
- MCI_STATUS 命令
- 順序節奏
- 節奏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675919"
---
# <a name="querying-and-setting-the-tempo"></a><span data-ttu-id="cc0ce-109">查詢及設定節奏</span><span class="sxs-lookup"><span data-stu-id="cc0ce-109">Querying and Setting the Tempo</span></span>

<span data-ttu-id="cc0ce-110">若要取出序列的節奏，請使用 [**mci \_ status**](mci-status.md)命令，並將 [**mci \_ status \_ PARMS**](mci-status-parms.md)結構的 **dwItem** 成員設定為 mci \_ SEQ \_ status \_ 節奏。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-110">To retrieve the tempo of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_TEMPO.</span></span> <span data-ttu-id="cc0ce-111">如果 **mci \_ status** 命令成功， **mci \_ status \_ PARMS** 結構的 **dwReturn** 成員就會包含目前的節奏。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure contains the current tempo.</span></span>

<span data-ttu-id="cc0ce-112">若要變更節奏，請使用 [**mci \_ set**](mci-set.md) 命令搭配 [**mci \_ seq \_ set \_ PARMS**](mci-seq-set-parms.md) 結構，指定 mci \_ seq \_ set 節奏旗標， \_ 並將結構的 **dwTempo** 成員設定為所需的節奏。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-112">To change tempo, use the [**MCI\_SET**](mci-set.md) command with the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, specifying the MCI\_SEQ\_SET\_TEMPO flag and setting the **dwTempo** member of the structure to the desired tempo.</span></span>

<span data-ttu-id="cc0ce-113">節奏的呈現方式視順序的除法類型而定。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-113">The way tempo is represented depends on the division type of the sequence.</span></span> <span data-ttu-id="cc0ce-114">如果除法類型是 PPQN，則節奏會以每分鐘的節拍表示。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-114">If the division type is PPQN, the tempo is represented in beats per minute.</span></span> <span data-ttu-id="cc0ce-115">如果除法類型是其中一個 SMPTE 除法類型，則節奏會以每秒的畫面格表示。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-115">If the division type is one of the SMPTE division types, the tempo is represented in frames per second.</span></span> <span data-ttu-id="cc0ce-116">如需決定序列之除法類型的詳細資訊，請參閱抓取 [序列除法類型](retrieving-the-sequence-division-type.md)。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-116">For information about determining the division type of a sequence, see [Retrieving the Sequence Division Type](retrieving-the-sequence-division-type.md).</span></span>

 

 




