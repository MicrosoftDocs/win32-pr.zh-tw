---
title: 接收 Time-Stamped 的 MIDI 訊息
description: 接收 Time-Stamped 的 MIDI 訊息
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- 音樂檢測數位介面 (MIDI) 、時間戳記訊息
- MIDI (音樂檢測數位介面) 、時間戳記訊息
- 錄製 MIDI 音訊、時間戳記訊息
- 時間戳記的 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314863"
---
# <a name="receiving-time-stamped-midi-messages"></a><span data-ttu-id="06f74-107">接收 Time-Stamped 的 MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="06f74-107">Receiving Time-Stamped MIDI Messages</span></span>

<span data-ttu-id="06f74-108">由於設備磁碟機接收 MIDI 訊息的時間與應用程式接收訊息的時間之間的延遲，因此，MIDI 輸入裝置磁碟機時間會將 MIDI 訊息加上訊息收到的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="06f74-108">Because of the delay between when the device driver receives a MIDI message and the time the application receives the message, MIDI input device drivers time stamp the MIDI message with the time that the message was received.</span></span> <span data-ttu-id="06f74-109">指定接收訊息第一個位元組時間的 MIDI 時間戳記（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="06f74-109">MIDI time stamps, which are defined as the time the first byte of the message was received, are specified in milliseconds.</span></span> <span data-ttu-id="06f74-110">[**MidiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)函式會將裝置的時間戳記重設為零。</span><span class="sxs-lookup"><span data-stu-id="06f74-110">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function resets the time stamps for a device to zero.</span></span>

<span data-ttu-id="06f74-111">如先前所述，若要接收具有 MIDI 輸入的時間戳記，您必須使用回呼函式。</span><span class="sxs-lookup"><span data-stu-id="06f74-111">As stated previously, to receive time stamps with MIDI input, you must use a callback function.</span></span> <span data-ttu-id="06f74-112">回呼函數的 *dwParam2* 參數會指定與 [**Mim \_ 資料**](mim-data.md) 和 [**mim \_ LONGDATA**](mim-longdata.md) 訊息相關聯之資料的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="06f74-112">The *dwParam2* parameter of the callback function specifies the time stamp for data associated with the [**MIM\_DATA**](mim-data.md) and [**MIM\_LONGDATA**](mim-longdata.md) messages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06f74-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="06f74-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06f74-114">錄製 MIDI 音訊</span><span class="sxs-lookup"><span data-stu-id="06f74-114">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 