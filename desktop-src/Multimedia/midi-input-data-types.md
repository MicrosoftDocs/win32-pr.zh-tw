---
title: MIDI 輸入資料類型
description: MIDI 輸入資料類型
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- 音樂檢測數位介面 (MIDI) 、輸入資料類型
- MIDI (的音樂檢測數位介面) 、輸入資料類型
- 錄製 MIDI 音訊，輸入資料類型
- MIDI 輸入資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968696"
---
# <a name="midi-input-data-types"></a><span data-ttu-id="de41f-107">MIDI 輸入資料類型</span><span class="sxs-lookup"><span data-stu-id="de41f-107">MIDI Input Data Types</span></span>

<span data-ttu-id="de41f-108">Windows 會為 MIDI 輸入函式定義下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="de41f-108">Windows defines the following data types for the MIDI input functions.</span></span>



| <span data-ttu-id="de41f-109">值</span><span class="sxs-lookup"><span data-stu-id="de41f-109">Value</span></span>                            | <span data-ttu-id="de41f-110">意義</span><span class="sxs-lookup"><span data-stu-id="de41f-110">Meaning</span></span>                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de41f-111">**HMIDIIN**</span><span class="sxs-lookup"><span data-stu-id="de41f-111">**HMIDIIN**</span></span>                      | <span data-ttu-id="de41f-112">MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="de41f-112">Handle of a MIDI input device.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="de41f-113">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="de41f-113">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | <span data-ttu-id="de41f-114">資料流程緩衝區或 MIDI 系統專屬資料區塊的標頭。</span><span class="sxs-lookup"><span data-stu-id="de41f-114">Header for a stream buffer or a block of MIDI system-exclusive data.</span></span> <span data-ttu-id="de41f-115">針對輸入應用程式，此結構只會記錄系統專屬的資料 (串流不支援 MIDI 輸入) 。</span><span class="sxs-lookup"><span data-stu-id="de41f-115">For input applications, this structure records only system-exclusive data (streaming is not supported for MIDI input).</span></span> |
| [<span data-ttu-id="de41f-116">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="de41f-116">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | <span data-ttu-id="de41f-117">用來查詢 MIDI 輸入裝置功能的結構。</span><span class="sxs-lookup"><span data-stu-id="de41f-117">Structure used to inquire about the capabilities of a MIDI input device.</span></span>                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="de41f-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="de41f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de41f-119">錄製 MIDI 音訊</span><span class="sxs-lookup"><span data-stu-id="de41f-119">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 