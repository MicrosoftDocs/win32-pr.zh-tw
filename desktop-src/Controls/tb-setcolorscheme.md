---
title: 'TB_SETCOLORSCHEME 訊息 (Commctrl .h) '
description: 設定工具列控制項的色彩配置資訊。
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844264"
---
# <a name="tb_setcolorscheme-message"></a><span data-ttu-id="89a13-104">TB \_ SETCOLORSCHEME 訊息</span><span class="sxs-lookup"><span data-stu-id="89a13-104">TB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="89a13-105">設定工具列控制項的色彩配置資訊。</span><span class="sxs-lookup"><span data-stu-id="89a13-105">Sets the color scheme information for the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="89a13-106">參數</span><span class="sxs-lookup"><span data-stu-id="89a13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89a13-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89a13-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="89a13-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="89a13-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="89a13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89a13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89a13-110">[**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme)結構的指標，其中包含色彩配置資訊。</span><span class="sxs-lookup"><span data-stu-id="89a13-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89a13-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="89a13-111">Return value</span></span>

<span data-ttu-id="89a13-112">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="89a13-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="89a13-113">備註</span><span class="sxs-lookup"><span data-stu-id="89a13-113">Remarks</span></span>

<span data-ttu-id="89a13-114">當您在控制項中繪製立體元素時，工具列控制項會使用色彩配置資訊。</span><span class="sxs-lookup"><span data-stu-id="89a13-114">The toolbar control uses the color scheme information when drawing the 3-D elements in the control.</span></span>

<span data-ttu-id="89a13-115">啟用視覺化樣式時，此訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="89a13-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="89a13-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="89a13-116">Requirements</span></span>



| <span data-ttu-id="89a13-117">需求</span><span class="sxs-lookup"><span data-stu-id="89a13-117">Requirement</span></span> | <span data-ttu-id="89a13-118">值</span><span class="sxs-lookup"><span data-stu-id="89a13-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89a13-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89a13-119">Minimum supported client</span></span><br/> | <span data-ttu-id="89a13-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89a13-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89a13-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89a13-121">Minimum supported server</span></span><br/> | <span data-ttu-id="89a13-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89a13-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89a13-123">標頭</span><span class="sxs-lookup"><span data-stu-id="89a13-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="89a13-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="89a13-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89a13-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89a13-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a13-126">**TB \_ GETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="89a13-126">**TB\_GETCOLORSCHEME**</span></span>](tb-getcolorscheme.md)
</dt> </dl>

 

 





