---
title: 'MCIWNDM_GETSTYLES 訊息 (Vfw .h) '
description: MCIWNDM \_ GETSTYLES 訊息會抓取指定視窗所使用之目前 MCIWnd 視窗樣式的旗標。 您可以使用 MCIWndGetStyles 宏明確地傳送此訊息。
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966953"
---
# <a name="mciwndm_getstyles-message"></a><span data-ttu-id="1debd-105">MCIWNDM \_ GETSTYLES 訊息</span><span class="sxs-lookup"><span data-stu-id="1debd-105">MCIWNDM\_GETSTYLES message</span></span>

<span data-ttu-id="1debd-106">**MCIWNDM \_ GETSTYLES** 訊息會抓取指定視窗所使用之目前 MCIWnd 視窗樣式的旗標。</span><span class="sxs-lookup"><span data-stu-id="1debd-106">The **MCIWNDM\_GETSTYLES** message retrieves the flags specifying the current MCIWnd window styles used by a window.</span></span> <span data-ttu-id="1debd-107">您可以使用 [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1debd-107">You can send this message explicitly or by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="1debd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1debd-108">Return Value</span></span>

<span data-ttu-id="1debd-109">傳回值，表示 MCIWnd 視窗目前的樣式。</span><span class="sxs-lookup"><span data-stu-id="1debd-109">Returns a value representing the current styles of the MCIWnd window.</span></span> <span data-ttu-id="1debd-110">傳回值是 MCIWnd 視窗樣式的位 OR 運算子， (MCIWNDF 旗標) 。</span><span class="sxs-lookup"><span data-stu-id="1debd-110">The return value is the bitwise OR operator of the MCIWnd window styles (MCIWNDF flags).</span></span>

## <a name="requirements"></a><span data-ttu-id="1debd-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1debd-111">Requirements</span></span>



| <span data-ttu-id="1debd-112">需求</span><span class="sxs-lookup"><span data-stu-id="1debd-112">Requirement</span></span> | <span data-ttu-id="1debd-113">值</span><span class="sxs-lookup"><span data-stu-id="1debd-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1debd-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1debd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1debd-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1debd-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1debd-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1debd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1debd-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1debd-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1debd-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1debd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1debd-119"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="1debd-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1debd-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1debd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1debd-121">**MCIWndGetStyles**</span><span class="sxs-lookup"><span data-stu-id="1debd-121">**MCIWndGetStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





