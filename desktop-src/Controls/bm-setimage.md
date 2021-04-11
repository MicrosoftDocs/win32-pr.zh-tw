---
title: 'BM_SETIMAGE 訊息 (Winuser .h) '
description: 將新影像 (圖示或點陣圖) 與按鈕產生關聯。
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094083"
---
# <a name="bm_setimage-message"></a><span data-ttu-id="445ce-104">BM \_ SETIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="445ce-104">BM\_SETIMAGE message</span></span>

<span data-ttu-id="445ce-105">將新影像 (圖示或點陣圖) 與按鈕產生關聯。</span><span class="sxs-lookup"><span data-stu-id="445ce-105">Associates a new image (icon or bitmap) with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="445ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="445ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="445ce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="445ce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="445ce-108">要與按鈕相關聯的影像類型。</span><span class="sxs-lookup"><span data-stu-id="445ce-108">The type of image to associate with the button.</span></span> <span data-ttu-id="445ce-109">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="445ce-109">This parameter can be one of the following values:</span></span>

-   <span data-ttu-id="445ce-110">影像 \_ 點陣圖</span><span class="sxs-lookup"><span data-stu-id="445ce-110">IMAGE\_BITMAP</span></span>
-   <span data-ttu-id="445ce-111">影像 \_ 圖示</span><span class="sxs-lookup"><span data-stu-id="445ce-111">IMAGE\_ICON</span></span>

</dd> <dt>

<span data-ttu-id="445ce-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="445ce-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="445ce-113"> (**HICON** 或) **HBITMAP** 的控制碼，以與按鈕相關聯的影像。</span><span class="sxs-lookup"><span data-stu-id="445ce-113">A handle (**HICON** or **HBITMAP**) to the image to associate with the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="445ce-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="445ce-114">Return value</span></span>

<span data-ttu-id="445ce-115">傳回值是先前與按鈕相關聯之影像的控制碼（如果有的話）。否則，它會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="445ce-115">The return value is a handle to the image previously associated with the button, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="445ce-116">備註</span><span class="sxs-lookup"><span data-stu-id="445ce-116">Remarks</span></span>

<span data-ttu-id="445ce-117">按鈕控制項上的文字、圖示或兩者的外觀取決於 [**BS \_ 圖示**](button-styles.md) 和 [**BS \_ 點陣圖**](button-styles.md) 樣式，以及是否呼叫 **BM \_ SETIMAGE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="445ce-117">The appearance of text, an icon, or both on a button control depends on the [**BS\_ICON**](button-styles.md) and [**BS\_BITMAP**](button-styles.md) styles, and whether the **BM\_SETIMAGE** message is called.</span></span> <span data-ttu-id="445ce-118">可能的結果如下所示：</span><span class="sxs-lookup"><span data-stu-id="445ce-118">The possible results are as follows:</span></span>



| <span data-ttu-id="445ce-119">BS \_ 圖示或 BS \_ 點陣圖集合？</span><span class="sxs-lookup"><span data-stu-id="445ce-119">BS\_ICON or BS\_BITMAP Set?</span></span> | <span data-ttu-id="445ce-120">\_呼叫 BM SETIMAGE？</span><span class="sxs-lookup"><span data-stu-id="445ce-120">BM\_SETIMAGE Called?</span></span> | <span data-ttu-id="445ce-121">結果</span><span class="sxs-lookup"><span data-stu-id="445ce-121">Result</span></span>              |
|-----------------------------|----------------------|---------------------|
| <span data-ttu-id="445ce-122">是</span><span class="sxs-lookup"><span data-stu-id="445ce-122">Yes</span></span>                         | <span data-ttu-id="445ce-123">是</span><span class="sxs-lookup"><span data-stu-id="445ce-123">Yes</span></span>                  | <span data-ttu-id="445ce-124">僅顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="445ce-124">Show icon only.</span></span>     |
| <span data-ttu-id="445ce-125">否</span><span class="sxs-lookup"><span data-stu-id="445ce-125">No</span></span>                          | <span data-ttu-id="445ce-126">是</span><span class="sxs-lookup"><span data-stu-id="445ce-126">Yes</span></span>                  | <span data-ttu-id="445ce-127">顯示圖示和文字。</span><span class="sxs-lookup"><span data-stu-id="445ce-127">Show icon and text.</span></span> |
| <span data-ttu-id="445ce-128">是</span><span class="sxs-lookup"><span data-stu-id="445ce-128">Yes</span></span>                         | <span data-ttu-id="445ce-129">否</span><span class="sxs-lookup"><span data-stu-id="445ce-129">No</span></span>                   | <span data-ttu-id="445ce-130">只顯示文字。</span><span class="sxs-lookup"><span data-stu-id="445ce-130">Show text only.</span></span>     |
| <span data-ttu-id="445ce-131">否</span><span class="sxs-lookup"><span data-stu-id="445ce-131">No</span></span>                          | <span data-ttu-id="445ce-132">否</span><span class="sxs-lookup"><span data-stu-id="445ce-132">No</span></span>                   | <span data-ttu-id="445ce-133">只顯示文字</span><span class="sxs-lookup"><span data-stu-id="445ce-133">Show text only</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="445ce-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="445ce-134">Requirements</span></span>



| <span data-ttu-id="445ce-135">需求</span><span class="sxs-lookup"><span data-stu-id="445ce-135">Requirement</span></span> | <span data-ttu-id="445ce-136">值</span><span class="sxs-lookup"><span data-stu-id="445ce-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="445ce-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="445ce-137">Minimum supported client</span></span><br/> | <span data-ttu-id="445ce-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="445ce-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="445ce-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="445ce-139">Minimum supported server</span></span><br/> | <span data-ttu-id="445ce-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="445ce-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="445ce-141">標頭</span><span class="sxs-lookup"><span data-stu-id="445ce-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="445ce-142"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="445ce-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="445ce-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="445ce-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445ce-144">**BM \_ GETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="445ce-144">**BM\_GETIMAGE**</span></span>](bm-getimage.md)
</dt> </dl>

 

 





