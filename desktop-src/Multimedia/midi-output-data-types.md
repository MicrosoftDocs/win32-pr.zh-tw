---
title: MIDI 輸出資料類型
description: MIDI 輸出資料類型
ms.assetid: d0cb0614-e979-4b9f-81ce-13457fdde906
keywords:
- 音樂檢測數位介面 (MIDI) ，輸出資料類型
- MIDI (的音樂檢測數位介面) ，輸出資料類型
- 播放 MIDI 檔案，輸出資料類型
- MIDI 輸出資料類型
- MIDIHDR 資料類型
- MIDIOUTCAPS 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57911800e0d45c1db515e5b57045aae3856732c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682114"
---
# <a name="midi-output-data-types"></a><span data-ttu-id="ce433-109">MIDI 輸出資料類型</span><span class="sxs-lookup"><span data-stu-id="ce433-109">MIDI Output Data Types</span></span>

<span data-ttu-id="ce433-110">Windows 會為 MIDI 輸出函式定義下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="ce433-110">Windows defines the following data types for MIDI output functions.</span></span>



| <span data-ttu-id="ce433-111">值</span><span class="sxs-lookup"><span data-stu-id="ce433-111">Value</span></span>                              | <span data-ttu-id="ce433-112">意義</span><span class="sxs-lookup"><span data-stu-id="ce433-112">Meaning</span></span>                                                                              |
|------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ce433-113">**HMIDIOUT**</span><span class="sxs-lookup"><span data-stu-id="ce433-113">**HMIDIOUT**</span></span>                       | <span data-ttu-id="ce433-114">MIDI 輸出裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ce433-114">Handle of a MIDI output device.</span></span>                                                      |
| [<span data-ttu-id="ce433-115">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="ce433-115">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)         | <span data-ttu-id="ce433-116">MIDI 系統專屬或串流資料區塊的標頭。</span><span class="sxs-lookup"><span data-stu-id="ce433-116">Header for a block of MIDI system-exclusive or stream data.</span></span>                          |
| [<span data-ttu-id="ce433-117">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="ce433-117">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) | <span data-ttu-id="ce433-118">用來查詢特定 MIDI 輸出裝置功能的結構。</span><span class="sxs-lookup"><span data-stu-id="ce433-118">Structure used to inquire about the capabilities of a particular MIDI output device.</span></span> |



 

 

 