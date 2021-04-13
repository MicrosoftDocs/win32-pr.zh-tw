---
title: 'RB_SETCOLORSCHEME 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的色彩配置資訊。
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- RB_SETCOLORSCHEME message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508699"
---
# <a name="rb_setcolorscheme-message"></a><span data-ttu-id="10b4f-104">RB \_ SETCOLORSCHEME 訊息</span><span class="sxs-lookup"><span data-stu-id="10b4f-104">RB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="10b4f-105">設定 Rebar 控制項的色彩配置資訊。</span><span class="sxs-lookup"><span data-stu-id="10b4f-105">Sets the color scheme information for the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="10b4f-106">參數</span><span class="sxs-lookup"><span data-stu-id="10b4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10b4f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="10b4f-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="10b4f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="10b4f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10b4f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10b4f-110">[**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme)結構的指標，其中包含色彩配置資訊。</span><span class="sxs-lookup"><span data-stu-id="10b4f-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b4f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="10b4f-111">Return value</span></span>

<span data-ttu-id="10b4f-112">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="10b4f-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="10b4f-113">備註</span><span class="sxs-lookup"><span data-stu-id="10b4f-113">Remarks</span></span>

<span data-ttu-id="10b4f-114">當您在控制項和區段中繪製立體元素時，Rebar 控制項會使用色彩配置資訊。</span><span class="sxs-lookup"><span data-stu-id="10b4f-114">The rebar control uses the color scheme information when drawing the 3-D elements in the control and bands.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b4f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="10b4f-115">Requirements</span></span>



| <span data-ttu-id="10b4f-116">需求</span><span class="sxs-lookup"><span data-stu-id="10b4f-116">Requirement</span></span> | <span data-ttu-id="10b4f-117">值</span><span class="sxs-lookup"><span data-stu-id="10b4f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10b4f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10b4f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10b4f-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10b4f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10b4f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10b4f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10b4f-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10b4f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10b4f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="10b4f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b4f-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="10b4f-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10b4f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10b4f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b4f-125">**RB \_ GETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="10b4f-125">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
</dt> </dl>

 

 





