---
title: 'MCIWNDM_PLAYFROM 訊息 (Vfw .h) '
description: MCIWNDM \_ PLAYFROM 訊息會從指定的位置，將 MCI 裝置的內容播放到內容的結尾，或直到另一個命令停止播放為止。 您可以使用 MCIWndPlayFrom 宏明確地傳送此訊息。
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- MCIWNDM_PLAYFROM message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934028"
---
# <a name="mciwndm_playfrom-message"></a><span data-ttu-id="5f867-105">MCIWNDM \_ PLAYFROM 訊息</span><span class="sxs-lookup"><span data-stu-id="5f867-105">MCIWNDM\_PLAYFROM message</span></span>

<span data-ttu-id="5f867-106">**MCIWNDM \_ PLAYFROM** 訊息會從指定的位置，將 MCI 裝置的內容播放到內容的結尾，或直到另一個命令停止播放為止。</span><span class="sxs-lookup"><span data-stu-id="5f867-106">The **MCIWNDM\_PLAYFROM** message plays the content of an MCI device from the specified location to the end of the content or until another command stops playback.</span></span> <span data-ttu-id="5f867-107">您可以使用 [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="5f867-107">You can send this message explicitly or by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span>


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a><span data-ttu-id="5f867-108">參數</span><span class="sxs-lookup"><span data-stu-id="5f867-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f867-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span><span class="sxs-lookup"><span data-stu-id="5f867-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span></span>
</dt> <dd>

<span data-ttu-id="5f867-110">開始位置。</span><span class="sxs-lookup"><span data-stu-id="5f867-110">Starting location.</span></span> <span data-ttu-id="5f867-111">起始位置的單位取決於目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="5f867-111">The units for the starting location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f867-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f867-112">Return Value</span></span>

<span data-ttu-id="5f867-113">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f867-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f867-114">備註</span><span class="sxs-lookup"><span data-stu-id="5f867-114">Remarks</span></span>

<span data-ttu-id="5f867-115">您也可以使用 [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) 宏來指定播放的開始和結束位置。</span><span class="sxs-lookup"><span data-stu-id="5f867-115">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f867-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f867-116">Requirements</span></span>



| <span data-ttu-id="5f867-117">需求</span><span class="sxs-lookup"><span data-stu-id="5f867-117">Requirement</span></span> | <span data-ttu-id="5f867-118">值</span><span class="sxs-lookup"><span data-stu-id="5f867-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f867-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f867-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f867-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f867-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5f867-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f867-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f867-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f867-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f867-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5f867-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f867-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f867-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f867-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f867-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f867-126">**MCIWndPlayFrom**</span><span class="sxs-lookup"><span data-stu-id="5f867-126">**MCIWndPlayFrom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[<span data-ttu-id="5f867-127">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="5f867-127">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





