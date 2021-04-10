---
title: 'MCIWNDM_SETREPEAT 訊息 (Vfw .h) '
description: MCIWNDM \_ SETREPEAT 訊息會設定與連續播放相關聯的重複旗標。
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843912"
---
# <a name="mciwndm_setrepeat-message"></a><span data-ttu-id="b7eeb-104">MCIWNDM \_ SETREPEAT 訊息</span><span class="sxs-lookup"><span data-stu-id="b7eeb-104">MCIWNDM\_SETREPEAT message</span></span>

<span data-ttu-id="b7eeb-105">**MCIWNDM \_ SETREPEAT** 訊息會設定與連續播放相關聯的重複旗標。</span><span class="sxs-lookup"><span data-stu-id="b7eeb-105">The **MCIWNDM\_SETREPEAT** message sets the repeat flag associated with continuous playback.</span></span> <span data-ttu-id="b7eeb-106">**MCIWNDM \_ SETREPEAT** 訊息會與 [MCI \_ PLAY](mci-play.md)命令搭配運作，以提供持續播放的迴圈。</span><span class="sxs-lookup"><span data-stu-id="b7eeb-106">The **MCIWNDM\_SETREPEAT** message works in conjunction with the [MCI\_PLAY](mci-play.md) command to provide a continuous playback loop.</span></span> <span data-ttu-id="b7eeb-107">您可以使用 [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b7eeb-107">You can send this message explicitly or by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro.</span></span>


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a><span data-ttu-id="b7eeb-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7eeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7eeb-109"><span id="f"></span><span id="F"></span>*F*</span><span class="sxs-lookup"><span data-stu-id="b7eeb-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="b7eeb-110">重複旗標的新狀態。</span><span class="sxs-lookup"><span data-stu-id="b7eeb-110">New state of the repeat flag.</span></span> <span data-ttu-id="b7eeb-111">指定 **TRUE** 以開啟連續播放。</span><span class="sxs-lookup"><span data-stu-id="b7eeb-111">Specify **TRUE** to turn on continuous playback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7eeb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7eeb-112">Return Value</span></span>

<span data-ttu-id="b7eeb-113">傳回零。</span><span class="sxs-lookup"><span data-stu-id="b7eeb-113">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7eeb-114">備註</span><span class="sxs-lookup"><span data-stu-id="b7eeb-114">Remarks</span></span>

<span data-ttu-id="b7eeb-115">目前，MCIAVI 是唯一支援連續播放的裝置。</span><span class="sxs-lookup"><span data-stu-id="b7eeb-115">Currently, MCIAVI is the only device that supports continuous playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7eeb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7eeb-116">Requirements</span></span>



| <span data-ttu-id="b7eeb-117">需求</span><span class="sxs-lookup"><span data-stu-id="b7eeb-117">Requirement</span></span> | <span data-ttu-id="b7eeb-118">值</span><span class="sxs-lookup"><span data-stu-id="b7eeb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b7eeb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7eeb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7eeb-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7eeb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b7eeb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7eeb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7eeb-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7eeb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b7eeb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b7eeb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7eeb-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7eeb-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7eeb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7eeb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7eeb-126">MCI \_ 播放</span><span class="sxs-lookup"><span data-stu-id="b7eeb-126">MCI\_PLAY</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="b7eeb-127">**MCIWndSetRepeat**</span><span class="sxs-lookup"><span data-stu-id="b7eeb-127">**MCIWndSetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





