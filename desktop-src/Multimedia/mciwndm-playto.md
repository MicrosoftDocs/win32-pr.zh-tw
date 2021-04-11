---
title: 'MCIWNDM_PLAYTO 訊息 (Vfw .h) '
description: MCIWNDM \_ PLAYTO 訊息會從目前位置將 MCI 裝置的內容播放到指定的結束位置，或直到另一個命令停止播放為止。
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105431"
---
# <a name="mciwndm_playto-message"></a><span data-ttu-id="4f94e-104">MCIWNDM \_ PLAYTO 訊息</span><span class="sxs-lookup"><span data-stu-id="4f94e-104">MCIWNDM\_PLAYTO message</span></span>

<span data-ttu-id="4f94e-105">**MCIWNDM \_ PLAYTO** 訊息會從目前位置將 MCI 裝置的內容播放到指定的結束位置，或直到另一個命令停止播放為止。</span><span class="sxs-lookup"><span data-stu-id="4f94e-105">The **MCIWNDM\_PLAYTO** message plays the content of an MCI device from the current position to the specified ending location or until another command stops playback.</span></span> <span data-ttu-id="4f94e-106">如果指定的結束位置超出內容的結尾，則會在內容結尾停止播放。</span><span class="sxs-lookup"><span data-stu-id="4f94e-106">If the specified ending location is beyond the end of the content, playback stops at the end of the content.</span></span> <span data-ttu-id="4f94e-107">您可以使用 [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4f94e-107">You can send this message explicitly or by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span>


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a><span data-ttu-id="4f94e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4f94e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f94e-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*借給*</span><span class="sxs-lookup"><span data-stu-id="4f94e-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*lEnd*</span></span>
</dt> <dd>

<span data-ttu-id="4f94e-110">結束位置。</span><span class="sxs-lookup"><span data-stu-id="4f94e-110">Ending location.</span></span> <span data-ttu-id="4f94e-111">結束位置的單位取決於目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="4f94e-111">The units for the ending location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f94e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f94e-112">Return Value</span></span>

<span data-ttu-id="4f94e-113">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f94e-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f94e-114">備註</span><span class="sxs-lookup"><span data-stu-id="4f94e-114">Remarks</span></span>

<span data-ttu-id="4f94e-115">這個宏是使用 [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) 和 [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) 宏來定義，接著使用 [MCI \_ SEEK](mci-seek.md) 命令和 **MCIWNDM \_ PLAYTO** 訊息。</span><span class="sxs-lookup"><span data-stu-id="4f94e-115">This macro is defined using the [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) and [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macros, which in turn use the [MCI\_SEEK](mci-seek.md) command and the **MCIWNDM\_PLAYTO** message.</span></span>

<span data-ttu-id="4f94e-116">您也可以使用 [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) 宏來指定播放的開始和結束位置。</span><span class="sxs-lookup"><span data-stu-id="4f94e-116">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f94e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f94e-117">Requirements</span></span>



| <span data-ttu-id="4f94e-118">需求</span><span class="sxs-lookup"><span data-stu-id="4f94e-118">Requirement</span></span> | <span data-ttu-id="4f94e-119">值</span><span class="sxs-lookup"><span data-stu-id="4f94e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4f94e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f94e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4f94e-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f94e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4f94e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f94e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4f94e-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f94e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4f94e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4f94e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f94e-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f94e-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f94e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f94e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f94e-127">MCI \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="4f94e-127">MCI\_SEEK</span></span>](mci-seek.md)
</dt> <dt>

[<span data-ttu-id="4f94e-128">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="4f94e-128">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[<span data-ttu-id="4f94e-129">**MCIWndPlayTo**</span><span class="sxs-lookup"><span data-stu-id="4f94e-129">**MCIWndPlayTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[<span data-ttu-id="4f94e-130">**MCIWndSeek**</span><span class="sxs-lookup"><span data-stu-id="4f94e-130">**MCIWndSeek**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





