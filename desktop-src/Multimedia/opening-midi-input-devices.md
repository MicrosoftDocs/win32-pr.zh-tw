---
title: 開啟 MIDI 輸入裝置
description: 開啟 MIDI 輸入裝置
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- 音樂檢測數位介面 (MIDI) 、輸入裝置
- MIDI (的音樂檢測數位介面) ，輸入裝置
- 錄製 MIDI 音訊、輸入裝置
- MIDI 輸入裝置
- " (MIDI) 的音樂檢測數位介面，開啟輸入裝置"
- MIDI (的音樂檢測數位介面) ，開啟輸入裝置
- 錄製 MIDI 音訊，開啟輸入裝置
- 開啟 MIDI 輸入裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682112"
---
# <a name="opening-midi-input-devices"></a><span data-ttu-id="fe101-111">開啟 MIDI 輸入裝置</span><span class="sxs-lookup"><span data-stu-id="fe101-111">Opening MIDI Input Devices</span></span>

<span data-ttu-id="fe101-112">若要開啟 MIDI 輸入裝置以進行錄製，請使用 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) 函式。</span><span class="sxs-lookup"><span data-stu-id="fe101-112">To open a MIDI input device for recording, use the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span> <span data-ttu-id="fe101-113">此函式會開啟與指定裝置識別碼相關聯的裝置，並將控制碼寫入指定的記憶體位置，以傳回開啟裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe101-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="fe101-114">如果您使用 [MIDI \_ IO \_ 狀態] 旗標搭配 **midiInOpen**，系統會使用 [**MIM \_ MOREDATA**](mim-moredata.md) 訊息來警示您的應用程式回呼函式，使其無法以足夠的速度處理 MIDI 資料來跟上輸入裝置磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fe101-114">If you use the MIDI\_IO\_STATUS flag with **midiInOpen**, the system uses the [**MIM\_MOREDATA**](mim-moredata.md) message to alert your application's callback function when it is not processing MIDI data fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="fe101-115"> ([**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md) 訊息會使用視窗回呼執行相同的作業。</span><span class="sxs-lookup"><span data-stu-id="fe101-115">(The [**MM\_MIM\_MOREDATA**](mm-mim-moredata.md) message does the same job with window callbacks.</span></span> <span data-ttu-id="fe101-116">不過，基於效能考慮，大部分的應用程式都會使用回呼函式，而不是使用視窗回呼。 ) 如果您的應用程式在個別的執行緒中處理 MIDI 資料，提高執行緒的優先順序可能會對應用程式與資料流程的能力有顯著的影響。</span><span class="sxs-lookup"><span data-stu-id="fe101-116">However, for performance reasons, most applications will use callback functions instead of window callbacks.) If your application processes MIDI data in a separate thread, boosting the thread's priority can have a significant impact on the application's ability to keep up with the data flow.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe101-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe101-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe101-118">錄製 MIDI 音訊</span><span class="sxs-lookup"><span data-stu-id="fe101-118">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 