---
title: 'EM_SETEDITSTYLEEX 訊息 (Richedit .h) '
description: 設定目前的擴充編輯樣式旗標。
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934911"
---
# <a name="em_seteditstyleex-message"></a><span data-ttu-id="75893-104">EM \_ SETEDITSTYLEEX 訊息</span><span class="sxs-lookup"><span data-stu-id="75893-104">EM\_SETEDITSTYLEEX message</span></span>

<span data-ttu-id="75893-105">設定目前的擴充編輯樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="75893-105">Sets the current extended edit style flags.</span></span>


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a><span data-ttu-id="75893-106">參數</span><span class="sxs-lookup"><span data-stu-id="75893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75893-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75893-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75893-108">指定一或多個擴充編輯樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="75893-108">Specifies one or more extended edit style flags.</span></span> <span data-ttu-id="75893-109">如需可能值的清單，請參閱 [**EM \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex)。</span><span class="sxs-lookup"><span data-stu-id="75893-109">For a list of possible values, see [**EM\_GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span></span>

</dd> <dt>

<span data-ttu-id="75893-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75893-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75893-111">由一或多個 *wParam* 值所組成的遮罩。</span><span class="sxs-lookup"><span data-stu-id="75893-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="75893-112">只會設定或清除此遮罩中指定的值。</span><span class="sxs-lookup"><span data-stu-id="75893-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="75893-113">這可讓您設定或清除單一旗標，而不需要讀取目前的旗標狀態。</span><span class="sxs-lookup"><span data-stu-id="75893-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75893-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="75893-114">Return value</span></span>

<span data-ttu-id="75893-115">當 rich edit 嘗試執行編輯樣式變更之後，傳回值即為擴充編輯樣式旗標的狀態。</span><span class="sxs-lookup"><span data-stu-id="75893-115">The return value is the state of the extended edit style flags after rich edit has attempted to implement your edit style changes.</span></span> <span data-ttu-id="75893-116">編輯樣式旗標是一組旗標，表示目前的編輯樣式。</span><span class="sxs-lookup"><span data-stu-id="75893-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="75893-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="75893-117">Requirements</span></span>



| <span data-ttu-id="75893-118">需求</span><span class="sxs-lookup"><span data-stu-id="75893-118">Requirement</span></span> | <span data-ttu-id="75893-119">值</span><span class="sxs-lookup"><span data-stu-id="75893-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75893-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75893-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75893-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75893-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="75893-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75893-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75893-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75893-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75893-124">標頭</span><span class="sxs-lookup"><span data-stu-id="75893-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75893-125"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="75893-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75893-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75893-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75893-127">**EM \_ GETEDITSTYLEEX**</span><span class="sxs-lookup"><span data-stu-id="75893-127">**EM\_GETEDITSTYLEEX**</span></span>](em-geteditstyleex.md)
</dt> </dl>

 

