---
title: 'EM_GETELLIPSISMODE 訊息 (Richedit .h) '
description: 抓取目前的省略號模式。
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103787"
---
# <a name="em_getellipsismode-message"></a><span data-ttu-id="54687-104">EM \_ GETELLIPSISMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="54687-104">EM\_GETELLIPSISMODE message</span></span>

<span data-ttu-id="54687-105">抓取目前的省略號模式。</span><span class="sxs-lookup"><span data-stu-id="54687-105">Retrieves the current ellipsis mode.</span></span> <span data-ttu-id="54687-106">啟用時，會針對不符合顯示視窗的文字顯示省略號 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="54687-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="54687-107">只有當控制項不在使用中時，才會使用省略號。</span><span class="sxs-lookup"><span data-stu-id="54687-107">The ellipsis is only used when the control is not active.</span></span> <span data-ttu-id="54687-108">使用中時，捲軸會用來顯示不符合顯示視窗的文字。</span><span class="sxs-lookup"><span data-stu-id="54687-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a><span data-ttu-id="54687-109">參數</span><span class="sxs-lookup"><span data-stu-id="54687-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54687-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54687-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54687-111">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="54687-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="54687-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54687-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54687-113">接收下列其中一個值的 DWORD 指標。</span><span class="sxs-lookup"><span data-stu-id="54687-113">Pointer to a DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="54687-114">值</span><span class="sxs-lookup"><span data-stu-id="54687-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="54687-115">意義</span><span class="sxs-lookup"><span data-stu-id="54687-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="54687-116"><dt>**省略號 \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="54687-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="54687-117">不使用省略號。</span><span class="sxs-lookup"><span data-stu-id="54687-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="54687-118"><dt>**省略號 \_ 結束**</dt></span><span class="sxs-lookup"><span data-stu-id="54687-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="54687-119">結束時的省略號 (強制中斷) 。</span><span class="sxs-lookup"><span data-stu-id="54687-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="54687-120"><dt>**省略號 \_ 單字**</dt></span><span class="sxs-lookup"><span data-stu-id="54687-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="54687-121">尾端的省略號 (斷詞) 。</span><span class="sxs-lookup"><span data-stu-id="54687-121">Ellipsis at the end (word break).</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54687-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="54687-122">Return value</span></span>

<span data-ttu-id="54687-123">如果 wparam 為0，而 lparam 不是 Null，則傳回值等於 TRUE;否則，傳回值等於 FALSE。</span><span class="sxs-lookup"><span data-stu-id="54687-123">If wparam is 0 and lparam is not NULL, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="54687-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="54687-124">Requirements</span></span>



| <span data-ttu-id="54687-125">需求</span><span class="sxs-lookup"><span data-stu-id="54687-125">Requirement</span></span> | <span data-ttu-id="54687-126">值</span><span class="sxs-lookup"><span data-stu-id="54687-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54687-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54687-127">Minimum supported client</span></span><br/> | <span data-ttu-id="54687-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54687-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="54687-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54687-129">Minimum supported server</span></span><br/> | <span data-ttu-id="54687-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54687-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54687-131">標頭</span><span class="sxs-lookup"><span data-stu-id="54687-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="54687-132"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="54687-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54687-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54687-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54687-134">**EM \_ SETELLIPSISMODE**</span><span class="sxs-lookup"><span data-stu-id="54687-134">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> <dt>

[<span data-ttu-id="54687-135">**EM \_ GETELLIPSISSTATE**</span><span class="sxs-lookup"><span data-stu-id="54687-135">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





