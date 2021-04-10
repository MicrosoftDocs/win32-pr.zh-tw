---
title: 設定時間格式
description: 設定時間格式
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET 命令訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842187"
---
# <a name="setting-the-time-format"></a><span data-ttu-id="9328c-104">設定時間格式</span><span class="sxs-lookup"><span data-stu-id="9328c-104">Setting the Time Format</span></span>

<span data-ttu-id="9328c-105">使用 [**mci \_ set**](mci-set.md) 命令訊息以及 [**mci \_ set \_ PARMS**](mci-set-parms.md) 結構來設定開啟裝置的時間格式。</span><span class="sxs-lookup"><span data-stu-id="9328c-105">Use the [**MCI\_SET**](mci-set.md) command message along with the [**MCI\_SET\_PARMS**](mci-set-parms.md) structure to set the time format for an open device.</span></span> <span data-ttu-id="9328c-106">將 **dwTimeFormat** 成員設定為下列其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="9328c-106">Set the **dwTimeFormat** member to one of the following constants.</span></span>



| <span data-ttu-id="9328c-107">常數</span><span class="sxs-lookup"><span data-stu-id="9328c-107">Constant</span></span>                   | <span data-ttu-id="9328c-108">時間格式</span><span class="sxs-lookup"><span data-stu-id="9328c-108">Time format</span></span>                                          |
|----------------------------|------------------------------------------------------|
| <span data-ttu-id="9328c-109">MCI \_ 格式 \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="9328c-109">MCI\_FORMAT\_BYTES</span></span>         | <span data-ttu-id="9328c-110">以脈衝程式碼調製 PCM 格式檔案 (的位元組 \[ \]) </span><span class="sxs-lookup"><span data-stu-id="9328c-110">Bytes (in pulse code modulated \[PCM\] format files)</span></span> |
| <span data-ttu-id="9328c-111">MCI \_ 格式 \_ 毫秒</span><span class="sxs-lookup"><span data-stu-id="9328c-111">MCI\_FORMAT\_MILLISECONDS</span></span>  | <span data-ttu-id="9328c-112">毫秒</span><span class="sxs-lookup"><span data-stu-id="9328c-112">Milliseconds</span></span>                                         |
| <span data-ttu-id="9328c-113">MCI \_ 格式 \_ MSF</span><span class="sxs-lookup"><span data-stu-id="9328c-113">MCI\_FORMAT\_MSF</span></span>           | <span data-ttu-id="9328c-114">分鐘/秒/框架</span><span class="sxs-lookup"><span data-stu-id="9328c-114">Minute/second/frame</span></span>                                  |
| <span data-ttu-id="9328c-115">MCI \_ 格式 \_ 範例</span><span class="sxs-lookup"><span data-stu-id="9328c-115">MCI\_FORMAT\_SAMPLES</span></span>       | <span data-ttu-id="9328c-116">範例</span><span class="sxs-lookup"><span data-stu-id="9328c-116">Samples</span></span>                                              |
| <span data-ttu-id="9328c-117">MCI \_ 格式的 \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="9328c-117">MCI\_FORMAT\_SMPTE\_24</span></span>     | <span data-ttu-id="9328c-118">SMPTE，24個框架</span><span class="sxs-lookup"><span data-stu-id="9328c-118">SMPTE, 24 frame</span></span>                                      |
| <span data-ttu-id="9328c-119">MCI \_ 格式的 \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="9328c-119">MCI\_FORMAT\_SMPTE\_25</span></span>     | <span data-ttu-id="9328c-120">SMPTE，25個框架</span><span class="sxs-lookup"><span data-stu-id="9328c-120">SMPTE, 25 frame</span></span>                                      |
| <span data-ttu-id="9328c-121">MCI \_ 格式 \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="9328c-121">MCI\_FORMAT\_SMPTE\_30</span></span>     | <span data-ttu-id="9328c-122">SMPTE，30個畫面格</span><span class="sxs-lookup"><span data-stu-id="9328c-122">SMPTE, 30 frame</span></span>                                      |
| <span data-ttu-id="9328c-123">MCI \_ 格式的 \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="9328c-123">MCI\_FORMAT\_SMPTE\_30DROP</span></span> | <span data-ttu-id="9328c-124">SMPTE，30個畫面格下降</span><span class="sxs-lookup"><span data-stu-id="9328c-124">SMPTE, 30 frame drop</span></span>                                 |
| <span data-ttu-id="9328c-125">MCI \_ 格式 \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="9328c-125">MCI\_FORMAT\_TMSF</span></span>          | <span data-ttu-id="9328c-126">曲目/分鐘/秒/畫面格</span><span class="sxs-lookup"><span data-stu-id="9328c-126">Track/minute/second/frame</span></span>                            |
| <span data-ttu-id="9328c-127">MCI \_ SEQ \_ 格式 \_ SONGPTR</span><span class="sxs-lookup"><span data-stu-id="9328c-127">MCI\_SEQ\_FORMAT\_SONGPTR</span></span>  | <span data-ttu-id="9328c-128">MIDI 歌曲指標</span><span class="sxs-lookup"><span data-stu-id="9328c-128">MIDI song pointer</span></span>                                    |



 

<span data-ttu-id="9328c-129">下列範例會使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數，將 wDeviceID 變數所指定裝置的時間格式設定為毫秒。</span><span class="sxs-lookup"><span data-stu-id="9328c-129">The following example sets the time format to milliseconds on the device specified by the wDeviceID variable using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 