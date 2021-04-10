---
title: 'MCIWNDM_GETACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ GETACTIVETIMER 訊息會抓取 MCIWnd 視窗為使用中視窗時所使用的更新期間。 您可以使用 MCIWndGetActiveTimer 宏明確地傳送此訊息。
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106530"
---
# <a name="mciwndm_getactivetimer-message"></a><span data-ttu-id="13a52-105">MCIWNDM \_ GETACTIVETIMER 訊息</span><span class="sxs-lookup"><span data-stu-id="13a52-105">MCIWNDM\_GETACTIVETIMER message</span></span>

<span data-ttu-id="13a52-106">**MCIWNDM \_ GETACTIVETIMER** 訊息會抓取 MCIWnd 視窗為使用中視窗時所使用的更新期間。</span><span class="sxs-lookup"><span data-stu-id="13a52-106">The **MCIWNDM\_GETACTIVETIMER** message retrieves the update period used when the MCIWnd window is the active window.</span></span> <span data-ttu-id="13a52-107">您可以使用 [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="13a52-107">You can send this message explicitly or by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span>


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="13a52-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="13a52-108">Return Value</span></span>

<span data-ttu-id="13a52-109">傳回更新期間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="13a52-109">Returns the update period in milliseconds.</span></span> <span data-ttu-id="13a52-110">預設值為500毫秒。</span><span class="sxs-lookup"><span data-stu-id="13a52-110">The default is 500 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a52-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="13a52-111">Requirements</span></span>



| <span data-ttu-id="13a52-112">需求</span><span class="sxs-lookup"><span data-stu-id="13a52-112">Requirement</span></span> | <span data-ttu-id="13a52-113">值</span><span class="sxs-lookup"><span data-stu-id="13a52-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13a52-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13a52-114">Minimum supported client</span></span><br/> | <span data-ttu-id="13a52-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13a52-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13a52-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13a52-116">Minimum supported server</span></span><br/> | <span data-ttu-id="13a52-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13a52-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13a52-118">標頭</span><span class="sxs-lookup"><span data-stu-id="13a52-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a52-119"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="13a52-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a52-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13a52-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a52-121">**MCIWndGetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="13a52-121">**MCIWndGetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





