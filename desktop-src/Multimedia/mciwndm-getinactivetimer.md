---
title: 'MCIWNDM_GETINACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ GETINACTIVETIMER 訊息會抓取 MCIWnd 視窗為非作用中視窗時所使用的更新期間。 您可以使用 MCIWndGetInactiveTimer 宏明確地傳送此訊息。
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969140"
---
# <a name="mciwndm_getinactivetimer-message"></a><span data-ttu-id="26ccc-105">MCIWNDM \_ GETINACTIVETIMER 訊息</span><span class="sxs-lookup"><span data-stu-id="26ccc-105">MCIWNDM\_GETINACTIVETIMER message</span></span>

<span data-ttu-id="26ccc-106">**MCIWNDM \_ GETINACTIVETIMER** 訊息會抓取 MCIWnd 視窗為非作用中視窗時所使用的更新期間。</span><span class="sxs-lookup"><span data-stu-id="26ccc-106">The **MCIWNDM\_GETINACTIVETIMER** message retrieves the update period used when the MCIWnd window is the inactive window.</span></span> <span data-ttu-id="26ccc-107">您可以使用 [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="26ccc-107">You can send this message explicitly or by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span>


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="26ccc-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="26ccc-108">Return Value</span></span>

<span data-ttu-id="26ccc-109">傳回更新期間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="26ccc-109">Returns the update period, in milliseconds.</span></span> <span data-ttu-id="26ccc-110">預設值為2000毫秒。</span><span class="sxs-lookup"><span data-stu-id="26ccc-110">The default value is 2000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="26ccc-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="26ccc-111">Requirements</span></span>



| <span data-ttu-id="26ccc-112">需求</span><span class="sxs-lookup"><span data-stu-id="26ccc-112">Requirement</span></span> | <span data-ttu-id="26ccc-113">值</span><span class="sxs-lookup"><span data-stu-id="26ccc-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="26ccc-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26ccc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="26ccc-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26ccc-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="26ccc-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26ccc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="26ccc-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26ccc-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="26ccc-118">標頭</span><span class="sxs-lookup"><span data-stu-id="26ccc-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="26ccc-119"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="26ccc-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ccc-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26ccc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ccc-121">**MCIWndGetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="26ccc-121">**MCIWndGetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





