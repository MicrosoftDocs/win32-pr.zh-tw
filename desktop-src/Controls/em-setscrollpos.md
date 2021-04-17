---
title: 'EM_SETSCROLLPOS 訊息 (Richedit .h) '
description: 將 rich edit 控制項的內容滾動至指定的點。
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466536"
---
# <a name="em_setscrollpos-message"></a><span data-ttu-id="2e731-104">EM \_ SETSCROLLPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="2e731-104">EM\_SETSCROLLPOS message</span></span>

<span data-ttu-id="2e731-105">將 rich edit 控制項的內容滾動至指定的點。</span><span class="sxs-lookup"><span data-stu-id="2e731-105">Scrolls the contents of a rich edit control to the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e731-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e731-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e731-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e731-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e731-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="2e731-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2e731-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e731-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e731-110">[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，指定檔之虛擬文字空間中的點（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e731-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure which specifies a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="2e731-111">檔將會被滾動，直到這個點位於 [編輯] 控制項視窗的左上角。</span><span class="sxs-lookup"><span data-stu-id="2e731-111">The document will be scrolled until this point is located in the upper-left corner of the edit control window.</span></span> <span data-ttu-id="2e731-112">如果您想要變更視圖，讓視圖的左上角是兩行向下，而左邊緣有一個字元。</span><span class="sxs-lookup"><span data-stu-id="2e731-112">If you want to change the view such that the upper left corner of the view is two lines down and one character in from the left edge.</span></span> <span data-ttu-id="2e731-113">您會傳遞 (7，22) 的點。</span><span class="sxs-lookup"><span data-stu-id="2e731-113">You would pass a point of (7, 22).</span></span>

<span data-ttu-id="2e731-114">Rich edit 控制項會檢查 x 和 y 座標，並視需要進行調整，以便在頂端顯示完整的行。</span><span class="sxs-lookup"><span data-stu-id="2e731-114">The rich edit control checks the x and y coordinates and adjusts them if necessary, so that a complete line is displayed at the top.</span></span> <span data-ttu-id="2e731-115">它也可確保文字永遠不會從 view 矩形中完整地滾動。</span><span class="sxs-lookup"><span data-stu-id="2e731-115">It also ensures that the text is never completely scrolled off the view rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e731-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e731-116">Return value</span></span>

<span data-ttu-id="2e731-117">此訊息一律會傳回1。</span><span class="sxs-lookup"><span data-stu-id="2e731-117">This message always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e731-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e731-118">Requirements</span></span>



| <span data-ttu-id="2e731-119">需求</span><span class="sxs-lookup"><span data-stu-id="2e731-119">Requirement</span></span> | <span data-ttu-id="2e731-120">值</span><span class="sxs-lookup"><span data-stu-id="2e731-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e731-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e731-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e731-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e731-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e731-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e731-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e731-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e731-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e731-125">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2e731-125">Redistributable</span></span><br/>          | <span data-ttu-id="2e731-126">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="2e731-126">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="2e731-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2e731-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e731-128"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e731-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e731-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e731-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e731-130">**EM \_ GETSCROLLPOS**</span><span class="sxs-lookup"><span data-stu-id="2e731-130">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> </dl>

 

