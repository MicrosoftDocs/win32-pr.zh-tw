---
title: 'EM_SETELLIPSISMODE 訊息 (Richedit .h) '
description: 這則訊息會設定目前的省略號模式。
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025386"
---
# <a name="em_setellipsismode-message"></a><span data-ttu-id="a24eb-104">EM \_ SETELLIPSISMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="a24eb-104">EM\_SETELLIPSISMODE message</span></span>

<span data-ttu-id="a24eb-105">這則訊息會設定目前的省略號模式。</span><span class="sxs-lookup"><span data-stu-id="a24eb-105">This message sets the current ellipsis mode.</span></span> <span data-ttu-id="a24eb-106">啟用時，會針對不符合顯示視窗的文字顯示省略號 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="a24eb-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="a24eb-107">只有當控制項不在作用中時，才會使用省略號。</span><span class="sxs-lookup"><span data-stu-id="a24eb-107">The ellipsis is only used when the control isn t active.</span></span> <span data-ttu-id="a24eb-108">使用中時，捲軸會用來顯示不符合顯示視窗的文字。</span><span class="sxs-lookup"><span data-stu-id="a24eb-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a><span data-ttu-id="a24eb-109">參數</span><span class="sxs-lookup"><span data-stu-id="a24eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24eb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a24eb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24eb-111">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="a24eb-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a24eb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a24eb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24eb-113">接受下列其中一個值的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="a24eb-113">A DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="a24eb-114">值</span><span class="sxs-lookup"><span data-stu-id="a24eb-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="a24eb-115">意義</span><span class="sxs-lookup"><span data-stu-id="a24eb-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="a24eb-116"><dt>**省略號 \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="a24eb-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="a24eb-117">不使用省略號。</span><span class="sxs-lookup"><span data-stu-id="a24eb-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="a24eb-118"><dt>**省略號 \_ 結束**</dt></span><span class="sxs-lookup"><span data-stu-id="a24eb-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="a24eb-119">結束時的省略號 (強制中斷) 。</span><span class="sxs-lookup"><span data-stu-id="a24eb-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="a24eb-120"><dt>**省略號 \_ 單字**</dt></span><span class="sxs-lookup"><span data-stu-id="a24eb-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="a24eb-121">尾端的省略號 (斷詞) 。</span><span class="sxs-lookup"><span data-stu-id="a24eb-121">Ellipsis at the end (word break).</span></span><br/>   |



 

<span data-ttu-id="a24eb-122">這些值的位都符合 **省略號 \_ 遮罩** 的大小。</span><span class="sxs-lookup"><span data-stu-id="a24eb-122">The bits for these values all fit in the **ELLIPSIS\_MASK**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24eb-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="a24eb-123">Return value</span></span>

<span data-ttu-id="a24eb-124">如果 wparam 為0，而 lparam 是上表中的其中一個值，則傳回值等於 TRUE;否則，傳回值等於 FALSE。</span><span class="sxs-lookup"><span data-stu-id="a24eb-124">If wparam is 0 and lparam is one of the values in the table above, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24eb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a24eb-125">Requirements</span></span>



| <span data-ttu-id="a24eb-126">需求</span><span class="sxs-lookup"><span data-stu-id="a24eb-126">Requirement</span></span> | <span data-ttu-id="a24eb-127">值</span><span class="sxs-lookup"><span data-stu-id="a24eb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a24eb-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a24eb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a24eb-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a24eb-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a24eb-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a24eb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a24eb-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a24eb-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a24eb-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a24eb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a24eb-133"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a24eb-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24eb-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a24eb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24eb-135">**EM \_ GETELLIPSISMODE**</span><span class="sxs-lookup"><span data-stu-id="a24eb-135">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="a24eb-136">**EM \_ GETELLIPSISSTATE**</span><span class="sxs-lookup"><span data-stu-id="a24eb-136">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





