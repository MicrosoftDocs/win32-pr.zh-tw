---
title: 'EM_GETELLIPSISSTATE 訊息 (Richedit .h) '
description: 抓取目前的省略號狀態。
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- EM_GETELLIPSISSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465385"
---
# <a name="em_getellipsisstate-message"></a><span data-ttu-id="2b183-104">EM \_ GETELLIPSISSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="2b183-104">EM\_GETELLIPSISSTATE message</span></span>

<span data-ttu-id="2b183-105">抓取目前的省略號狀態。</span><span class="sxs-lookup"><span data-stu-id="2b183-105">Retrieves the current ellipsis state.</span></span>


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a><span data-ttu-id="2b183-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b183-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b183-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b183-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="2b183-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2b183-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b183-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b183-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="2b183-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b183-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b183-111">Return value</span></span>

<span data-ttu-id="2b183-112">如果顯示省略號，則傳回值為 TRUE，否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="2b183-112">The return value is TRUE if an ellipsis is being displayed and FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b183-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b183-113">Requirements</span></span>



| <span data-ttu-id="2b183-114">需求</span><span class="sxs-lookup"><span data-stu-id="2b183-114">Requirement</span></span> | <span data-ttu-id="2b183-115">值</span><span class="sxs-lookup"><span data-stu-id="2b183-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b183-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b183-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2b183-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b183-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2b183-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b183-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2b183-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b183-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b183-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2b183-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b183-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b183-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b183-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b183-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b183-123">**EM \_ GETELLIPSISMODE**</span><span class="sxs-lookup"><span data-stu-id="2b183-123">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="2b183-124">**EM \_ SETELLIPSISMODE**</span><span class="sxs-lookup"><span data-stu-id="2b183-124">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> </dl>

 

 





