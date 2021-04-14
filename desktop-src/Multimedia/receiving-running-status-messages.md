---
title: 接收 Running-Status 訊息
description: 接收 Running-Status 訊息
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- 音樂檢測數位介面 (MIDI) ，執行狀態
- MIDI (音樂檢測數位介面) ，執行狀態
- 正在錄製 MIDI 音訊，執行狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371889"
---
# <a name="receiving-running-status-messages"></a><span data-ttu-id="f0f85-106">接收 Running-Status 訊息</span><span class="sxs-lookup"><span data-stu-id="f0f85-106">Receiving Running-Status Messages</span></span>

<span data-ttu-id="f0f85-107">*標準的 MIDI 檔案 1.0* 規格允許在訊息與先前的訊息具有相同的狀態位元組時，使用執行中的 *狀態*。</span><span class="sxs-lookup"><span data-stu-id="f0f85-107">The *Standard MIDI Files 1.0* specification allows the use of *running status* when a message has the same status byte as the previous message.</span></span> <span data-ttu-id="f0f85-108">使用執行狀態時，可以省略後續訊息的狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="f0f85-108">When running status is used, the status byte of subsequent messages can be omitted.</span></span> <span data-ttu-id="f0f85-109">所有的 MIDI 輸入裝置磁碟機都需要將使用執行中狀態的訊息擴充到完整的訊息中，如此一來，您一律會收到來自 MIDI 輸入裝置磁碟機的完整 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="f0f85-109">All MIDI input device drivers are required to expand messages using running status into complete messages, so that you always receive complete MIDI messages from a MIDI input device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0f85-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0f85-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0f85-111">錄製 MIDI 音訊</span><span class="sxs-lookup"><span data-stu-id="f0f85-111">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 




