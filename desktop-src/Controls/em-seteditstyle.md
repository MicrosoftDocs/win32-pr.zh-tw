---
title: 'EM_SETEDITSTYLE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的目前編輯樣式旗標。
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509171"
---
# <a name="em_seteditstyle-message"></a><span data-ttu-id="183fa-104">EM \_ SETEDITSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="183fa-104">EM\_SETEDITSTYLE message</span></span>

<span data-ttu-id="183fa-105">設定 rich edit 控制項的目前編輯樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="183fa-105">Sets the current edit style flags for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="183fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="183fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="183fa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="183fa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="183fa-108">指定一或多個編輯樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="183fa-108">Specifies one or more edit style flags.</span></span> <span data-ttu-id="183fa-109">如需可能值的清單，請參閱 [**EM \_ GETEDITSTYLE**](em-geteditstyle.md)。</span><span class="sxs-lookup"><span data-stu-id="183fa-109">For a list of possible values, see [**EM\_GETEDITSTYLE**](em-geteditstyle.md).</span></span>

</dd> <dt>

<span data-ttu-id="183fa-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="183fa-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="183fa-111">由一或多個 *wParam* 值所組成的遮罩。</span><span class="sxs-lookup"><span data-stu-id="183fa-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="183fa-112">只會設定或清除此遮罩中指定的值。</span><span class="sxs-lookup"><span data-stu-id="183fa-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="183fa-113">這可讓您設定或清除單一旗標，而不需要讀取目前的旗標狀態。</span><span class="sxs-lookup"><span data-stu-id="183fa-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="183fa-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="183fa-114">Return value</span></span>

<span data-ttu-id="183fa-115">當 rich edit 控制項嘗試執行編輯樣式變更之後，傳回值即為編輯樣式旗標的狀態。</span><span class="sxs-lookup"><span data-stu-id="183fa-115">The return value is the state of the edit style flags after the rich edit control has attempted to implement your edit style changes.</span></span> <span data-ttu-id="183fa-116">編輯樣式旗標是一組旗標，表示目前的編輯樣式。</span><span class="sxs-lookup"><span data-stu-id="183fa-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="183fa-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="183fa-117">Requirements</span></span>



| <span data-ttu-id="183fa-118">需求</span><span class="sxs-lookup"><span data-stu-id="183fa-118">Requirement</span></span> | <span data-ttu-id="183fa-119">值</span><span class="sxs-lookup"><span data-stu-id="183fa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="183fa-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="183fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="183fa-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="183fa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="183fa-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="183fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="183fa-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="183fa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="183fa-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="183fa-124">Redistributable</span></span><br/>          | <span data-ttu-id="183fa-125">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="183fa-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="183fa-126">標頭</span><span class="sxs-lookup"><span data-stu-id="183fa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="183fa-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="183fa-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="183fa-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="183fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="183fa-129">**EM \_ GETEDITSTYLE**</span><span class="sxs-lookup"><span data-stu-id="183fa-129">**EM\_GETEDITSTYLE**</span></span>](em-geteditstyle.md)
</dt> </dl>

 

 





