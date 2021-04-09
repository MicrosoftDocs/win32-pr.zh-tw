---
title: 'EM_DISPLAYBAND 訊息 (Richedit .h) '
description: 顯示 rich edit 控制項的部分內容，如先前使用 EM FORMATRANGE 訊息針對裝置格式化的部分 \_ 。
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND message Windows 控制項
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934635"
---
# <a name="em_displayband-message"></a><span data-ttu-id="1ccaa-104">EM \_ DISPLAYBAND 訊息</span><span class="sxs-lookup"><span data-stu-id="1ccaa-104">EM\_DISPLAYBAND message</span></span>

<span data-ttu-id="1ccaa-105">顯示 rich edit 控制項的部分內容，如先前使用 [**EM \_ FORMATRANGE**](em-formatrange.md) 訊息針對裝置格式化的部分。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-105">Displays a portion of the contents of a rich edit control, as previously formatted for a device using the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ccaa-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ccaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ccaa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ccaa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ccaa-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1ccaa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ccaa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ccaa-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構，指定裝置的顯示區域。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-110">A [**RECT**](/previous-versions//dd162897(v=vs.85)) structure specifying the display area of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ccaa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ccaa-111">Return value</span></span>

<span data-ttu-id="1ccaa-112">如果作業成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-112">If the operation succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="1ccaa-113">如果作業失敗，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-113">If the operation fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ccaa-114">備註</span><span class="sxs-lookup"><span data-stu-id="1ccaa-114">Remarks</span></span>

<span data-ttu-id="1ccaa-115">矩形會裁剪 (COM) 物件的文字和元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-115">Text and Component Object Model (COM) objects are clipped by the rectangle.</span></span> <span data-ttu-id="1ccaa-116">應用程式不需要設定裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-116">The application does not need to set the clipping region.</span></span>

<span data-ttu-id="1ccaa-117">「群組」是使用一或多個不同的矩形或群組來產生單一輸出頁面的處理常式。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-117">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="1ccaa-118">當所有條紋都放在頁面上時，就會產生完整的影像結果。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-118">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="1ccaa-119">這種方法通常是由沒有足夠記憶體的點陣印表機，或一次影像一整頁的功能所使用。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-119">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span> <span data-ttu-id="1ccaa-120">條紋裝置包含大部分的點矩陣印表機以及某些雷射印表機。</span><span class="sxs-lookup"><span data-stu-id="1ccaa-120">Banding devices include most dot matrix printers as well as some laser printers.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ccaa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ccaa-121">Requirements</span></span>



| <span data-ttu-id="1ccaa-122">需求</span><span class="sxs-lookup"><span data-stu-id="1ccaa-122">Requirement</span></span> | <span data-ttu-id="1ccaa-123">值</span><span class="sxs-lookup"><span data-stu-id="1ccaa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccaa-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ccaa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1ccaa-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ccaa-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ccaa-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ccaa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1ccaa-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ccaa-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ccaa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1ccaa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ccaa-129"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ccaa-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ccaa-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ccaa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ccaa-131">列印 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="1ccaa-131">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

