---
title: MIDI Sequencer 命令集
description: MIDI Sequencer 命令集
ms.assetid: 8f5af706-0674-4ed1-855f-22f8d74361fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bac1f9ca26a8e7e7e636c19ffa92d05281e16bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932155"
---
# <a name="midi-sequencer-command-set"></a><span data-ttu-id="de2d0-103">MIDI Sequencer 命令集</span><span class="sxs-lookup"><span data-stu-id="de2d0-103">MIDI Sequencer Command Set</span></span>

<span data-ttu-id="de2d0-104">MIDI sequencer 支援下列一組命令。</span><span class="sxs-lookup"><span data-stu-id="de2d0-104">The MIDI sequencer supports the following set of commands.</span></span>



| <span data-ttu-id="de2d0-105">字串形式</span><span class="sxs-lookup"><span data-stu-id="de2d0-105">String form</span></span>                      | <span data-ttu-id="de2d0-106">訊息表單</span><span class="sxs-lookup"><span data-stu-id="de2d0-106">Message form</span></span>                              |
|----------------------------------|-------------------------------------------|
| [<span data-ttu-id="de2d0-107">**打破**</span><span class="sxs-lookup"><span data-stu-id="de2d0-107">**break**</span></span>](break.md)           | [<span data-ttu-id="de2d0-108">**MCI \_ 斷路**</span><span class="sxs-lookup"><span data-stu-id="de2d0-108">**MCI\_BREAK**</span></span>](mci-break.md)           |
| [<span data-ttu-id="de2d0-109">**能力**</span><span class="sxs-lookup"><span data-stu-id="de2d0-109">**capability**</span></span>](capability.md) | [<span data-ttu-id="de2d0-110">**MCI \_ GETDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="de2d0-110">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md) |
| [<span data-ttu-id="de2d0-111">**關閉**</span><span class="sxs-lookup"><span data-stu-id="de2d0-111">**close**</span></span>](close.md)           | [<span data-ttu-id="de2d0-112">**MCI \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="de2d0-112">**MCI\_CLOSE**</span></span>](mci-close.md)           |
| [<span data-ttu-id="de2d0-113">**資訊**</span><span class="sxs-lookup"><span data-stu-id="de2d0-113">**info**</span></span>](info.md)             | [<span data-ttu-id="de2d0-114">**MCI \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="de2d0-114">**MCI\_INFO**</span></span>](mci-info.md)             |
| [<span data-ttu-id="de2d0-115">**打開**</span><span class="sxs-lookup"><span data-stu-id="de2d0-115">**open**</span></span>](open.md)             | [<span data-ttu-id="de2d0-116">**開啟的 MCI \_**</span><span class="sxs-lookup"><span data-stu-id="de2d0-116">**MCI\_OPEN**</span></span>](mci-open.md)             |
| [<span data-ttu-id="de2d0-117">**暫停**</span><span class="sxs-lookup"><span data-stu-id="de2d0-117">**pause**</span></span>](pause.md)           | [<span data-ttu-id="de2d0-118">**MCI \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="de2d0-118">**MCI\_PAUSE**</span></span>](mci-pause.md)           |
| [<span data-ttu-id="de2d0-119">**玩**</span><span class="sxs-lookup"><span data-stu-id="de2d0-119">**play**</span></span>](play.md)             | [<span data-ttu-id="de2d0-120">**MCI \_ 播放**</span><span class="sxs-lookup"><span data-stu-id="de2d0-120">**MCI\_PLAY**</span></span>](mci-play.md)             |
| [<span data-ttu-id="de2d0-121">**記錄**</span><span class="sxs-lookup"><span data-stu-id="de2d0-121">**record**</span></span>](record.md)         | [<span data-ttu-id="de2d0-122">**MCI \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="de2d0-122">**MCI\_RECORD**</span></span>](mci-record.md)         |
| [<span data-ttu-id="de2d0-123">**恢復**</span><span class="sxs-lookup"><span data-stu-id="de2d0-123">**resume**</span></span>](resume.md)         | [<span data-ttu-id="de2d0-124">**MCI \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="de2d0-124">**MCI\_RESUME**</span></span>](mci-resume.md)         |
| [<span data-ttu-id="de2d0-125">**救**</span><span class="sxs-lookup"><span data-stu-id="de2d0-125">**save**</span></span>](save.md)             | [<span data-ttu-id="de2d0-126">**MCI \_ 儲存**</span><span class="sxs-lookup"><span data-stu-id="de2d0-126">**MCI\_SAVE**</span></span>](mci-save.md)             |
| [<span data-ttu-id="de2d0-127">**尋求**</span><span class="sxs-lookup"><span data-stu-id="de2d0-127">**seek**</span></span>](seek.md)             | [<span data-ttu-id="de2d0-128">**MCI \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="de2d0-128">**MCI\_SEEK**</span></span>](mci-seek.md)             |
| [<span data-ttu-id="de2d0-129">**設置**</span><span class="sxs-lookup"><span data-stu-id="de2d0-129">**set**</span></span>](set.md)               | [<span data-ttu-id="de2d0-130">**MCI \_ 組**</span><span class="sxs-lookup"><span data-stu-id="de2d0-130">**MCI\_SET**</span></span>](mci-set.md)               |
| [<span data-ttu-id="de2d0-131">**地位**</span><span class="sxs-lookup"><span data-stu-id="de2d0-131">**status**</span></span>](status.md)         | [<span data-ttu-id="de2d0-132">**MCI \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="de2d0-132">**MCI\_STATUS**</span></span>](mci-status.md)         |
| [<span data-ttu-id="de2d0-133">**停止**</span><span class="sxs-lookup"><span data-stu-id="de2d0-133">**stop**</span></span>](stop.md)             | [<span data-ttu-id="de2d0-134">**MCI \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="de2d0-134">**MCI\_STOP**</span></span>](mci-stop.md)             |
| [<span data-ttu-id="de2d0-135">sysinfo</span><span class="sxs-lookup"><span data-stu-id="de2d0-135">sysinfo</span></span>](sysinfo.md)           | [<span data-ttu-id="de2d0-136">**MCI \_ SYSINFO**</span><span class="sxs-lookup"><span data-stu-id="de2d0-136">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)       |



 

 

 




