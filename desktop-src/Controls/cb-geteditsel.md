---
title: 'CB_GETEDITSEL 訊息 (Winuser .h) '
description: 取得下拉式方塊的編輯控制項中目前選取範圍的開始和結束字元位置。
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- CB_GETEDITSEL message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025093"
---
# <a name="cb_geteditsel-message"></a><span data-ttu-id="0d105-104">CB \_ GETEDITSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="0d105-104">CB\_GETEDITSEL message</span></span>

<span data-ttu-id="0d105-105">取得下拉式方塊的編輯控制項中目前選取範圍的開始和結束字元位置。</span><span class="sxs-lookup"><span data-stu-id="0d105-105">Gets the starting and ending character positions of the current selection in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d105-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d105-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d105-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d105-108">**DWORD** 值的指標，此值會接收選取範圍的開始位置。</span><span class="sxs-lookup"><span data-stu-id="0d105-108">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="0d105-109">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0d105-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0d105-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d105-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d105-111">**DWORD** 值的指標，此值會接收選取範圍的結束位置。</span><span class="sxs-lookup"><span data-stu-id="0d105-111">A pointer to a **DWORD** value that receives the ending position of the selection.</span></span> <span data-ttu-id="0d105-112">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0d105-112">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d105-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d105-113">Return value</span></span>

<span data-ttu-id="0d105-114">傳回值是以零為起始的 **DWORD** 值，其中包含在 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中選取範圍的開始位置，以及在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中最後一個選取的字元之後的第一個字元結束位置。</span><span class="sxs-lookup"><span data-stu-id="0d105-114">The return value is a zero-based **DWORD** value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and with the ending position of the first character after the last selected character in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="0d105-115">範例</span><span class="sxs-lookup"><span data-stu-id="0d105-115">Examples</span></span>

<span data-ttu-id="0d105-116">下列程式碼範例顯示兩種方法來抓取目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="0d105-116">The following code example shows two ways of retrieving the current selection range.</span></span>


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a><span data-ttu-id="0d105-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d105-117">Requirements</span></span>



| <span data-ttu-id="0d105-118">需求</span><span class="sxs-lookup"><span data-stu-id="0d105-118">Requirement</span></span> | <span data-ttu-id="0d105-119">值</span><span class="sxs-lookup"><span data-stu-id="0d105-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d105-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d105-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d105-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d105-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0d105-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d105-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d105-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d105-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0d105-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0d105-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d105-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0d105-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d105-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d105-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d105-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="0d105-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0d105-128">**CB \_ SETEDITSEL**</span><span class="sxs-lookup"><span data-stu-id="0d105-128">**CB\_SETEDITSEL**</span></span>](cb-seteditsel.md)
</dt> <dt>

<span data-ttu-id="0d105-129">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="0d105-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0d105-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d105-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0d105-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d105-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

