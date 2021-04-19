---
title: 'TB_SETBUTTONSIZE 訊息 (Commctrl .h) '
description: 設定工具列上的按鈕大小。
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967737"
---
# <a name="tb_setbuttonsize-message"></a><span data-ttu-id="a3131-104">TB \_ SETBUTTONSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="a3131-104">TB\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="a3131-105">設定工具列上的按鈕大小。</span><span class="sxs-lookup"><span data-stu-id="a3131-105">Sets the size of buttons on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3131-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3131-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3131-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3131-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3131-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a3131-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a3131-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3131-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3131-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定按鈕的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a3131-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the buttons.</span></span> <span data-ttu-id="a3131-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定按鈕的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a3131-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3131-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3131-112">Return value</span></span>

<span data-ttu-id="a3131-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a3131-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3131-114">備註</span><span class="sxs-lookup"><span data-stu-id="a3131-114">Remarks</span></span>

<span data-ttu-id="a3131-115">**TB \_** 您通常應該在加入按鈕之後呼叫 SETBUTTONSIZE。</span><span class="sxs-lookup"><span data-stu-id="a3131-115">**TB\_SETBUTTONSIZE** should generally be called after adding buttons.</span></span>

<span data-ttu-id="a3131-116">使用 [ [**TB] \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) 可設定按鈕在新增之前允許的最大寬度和最小值。</span><span class="sxs-lookup"><span data-stu-id="a3131-116">Use [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="a3131-117">使用 **TB \_ SETBUTTONSIZE** 來設定按鈕的實際大小。</span><span class="sxs-lookup"><span data-stu-id="a3131-117">Use **TB\_SETBUTTONSIZE** to set the actual size of buttons.</span></span>

## <a name="examples"></a><span data-ttu-id="a3131-118">範例</span><span class="sxs-lookup"><span data-stu-id="a3131-118">Examples</span></span>

<span data-ttu-id="a3131-119">下列程式碼範例會將按鈕的寬度設定為80圖元，並將高度設定為30圖元。</span><span class="sxs-lookup"><span data-stu-id="a3131-119">The following example code sets the width of buttons to 80 pixels and the height to 30 pixels.</span></span>


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a><span data-ttu-id="a3131-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3131-120">Requirements</span></span>



| <span data-ttu-id="a3131-121">需求</span><span class="sxs-lookup"><span data-stu-id="a3131-121">Requirement</span></span> | <span data-ttu-id="a3131-122">值</span><span class="sxs-lookup"><span data-stu-id="a3131-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3131-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3131-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a3131-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3131-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3131-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3131-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a3131-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3131-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3131-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a3131-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3131-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3131-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

