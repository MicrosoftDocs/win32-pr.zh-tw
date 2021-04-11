---
title: 'MCIWNDM_SETACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ SETACTIVETIMER 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新在視窗標題列中顯示的位置資訊，以及在 MCIWnd 視窗為使用中時將通知訊息傳送至父視窗的更新期間。 您可以使用 MCIWndSetActiveTimer 宏明確地傳送此訊息。
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104712"
---
# <a name="mciwndm_setactivetimer-message"></a><span data-ttu-id="ba91f-105">MCIWNDM \_ SETACTIVETIMER 訊息</span><span class="sxs-lookup"><span data-stu-id="ba91f-105">MCIWNDM\_SETACTIVETIMER message</span></span>

<span data-ttu-id="ba91f-106">**MCIWNDM \_ SETACTIVETIMER** 訊息會設定 MCIWnd 用來更新 [MCIWnd] 視窗中的提要欄位、更新在視窗標題列中顯示的位置資訊，以及在 MCIWnd 視窗為使用中時將通知訊息傳送至父視窗的更新期間。</span><span class="sxs-lookup"><span data-stu-id="ba91f-106">The **MCIWNDM\_SETACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active.</span></span> <span data-ttu-id="ba91f-107">您可以使用 [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ba91f-107">You can send this message explicitly or by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span>


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="ba91f-108">參數</span><span class="sxs-lookup"><span data-stu-id="ba91f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba91f-109"><span id="active"></span><span id="ACTIVE"></span>*積極*</span><span class="sxs-lookup"><span data-stu-id="ba91f-109"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="ba91f-110">更新期間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ba91f-110">Update period, in milliseconds.</span></span> <span data-ttu-id="ba91f-111">預設值為500毫秒。</span><span class="sxs-lookup"><span data-stu-id="ba91f-111">The default is 500 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba91f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba91f-112">Return Value</span></span>

<span data-ttu-id="ba91f-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ba91f-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba91f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba91f-114">Requirements</span></span>



| <span data-ttu-id="ba91f-115">需求</span><span class="sxs-lookup"><span data-stu-id="ba91f-115">Requirement</span></span> | <span data-ttu-id="ba91f-116">值</span><span class="sxs-lookup"><span data-stu-id="ba91f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ba91f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba91f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ba91f-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba91f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ba91f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba91f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ba91f-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba91f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ba91f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ba91f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba91f-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba91f-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba91f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba91f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba91f-124">**MCIWndSetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="ba91f-124">**MCIWndSetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





