---
title: 'MCIWNDM_GETREPEAT 訊息 (Vfw .h) '
description: MCIWNDM \_ GETREPEAT 訊息會判斷是否已啟用連續播放。 您可以使用 MCIWndGetRepeat 宏明確地傳送此訊息。
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- MCIWNDM_GETREPEAT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093999"
---
# <a name="mciwndm_getrepeat-message"></a><span data-ttu-id="741be-105">MCIWNDM \_ GETREPEAT 訊息</span><span class="sxs-lookup"><span data-stu-id="741be-105">MCIWNDM\_GETREPEAT message</span></span>

<span data-ttu-id="741be-106">**MCIWNDM \_ GETREPEAT** 訊息會判斷是否已啟用連續播放。</span><span class="sxs-lookup"><span data-stu-id="741be-106">The **MCIWNDM\_GETREPEAT** message determines if continuous playback has been activated.</span></span> <span data-ttu-id="741be-107">您可以使用 [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="741be-107">You can send this message explicitly or by using the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="741be-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="741be-108">Return Value</span></span>

<span data-ttu-id="741be-109">如果啟用連續播放則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="741be-109">Returns **TRUE** if continuous playback is activated or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="741be-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="741be-110">Requirements</span></span>



| <span data-ttu-id="741be-111">需求</span><span class="sxs-lookup"><span data-stu-id="741be-111">Requirement</span></span> | <span data-ttu-id="741be-112">值</span><span class="sxs-lookup"><span data-stu-id="741be-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="741be-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="741be-113">Minimum supported client</span></span><br/> | <span data-ttu-id="741be-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="741be-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="741be-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="741be-115">Minimum supported server</span></span><br/> | <span data-ttu-id="741be-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="741be-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="741be-117">標頭</span><span class="sxs-lookup"><span data-stu-id="741be-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="741be-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="741be-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="741be-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="741be-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741be-120">**MCIWndGetRepeat**</span><span class="sxs-lookup"><span data-stu-id="741be-120">**MCIWndGetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





