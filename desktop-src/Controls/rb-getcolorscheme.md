---
title: 'RB_GETCOLORSCHEME 訊息 (Commctrl .h) '
description: 從 Rebar 控制項抓取色彩配置資訊。
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- RB_GETCOLORSCHEME message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d154fd14b93127aa22148f2882f70018225cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508908"
---
# <a name="rb_getcolorscheme-message"></a><span data-ttu-id="32a13-104">RB \_ GETCOLORSCHEME 訊息</span><span class="sxs-lookup"><span data-stu-id="32a13-104">RB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="32a13-105">從 Rebar 控制項抓取色彩配置資訊。</span><span class="sxs-lookup"><span data-stu-id="32a13-105">Retrieves the color scheme information from the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="32a13-106">參數</span><span class="sxs-lookup"><span data-stu-id="32a13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32a13-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32a13-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="32a13-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="32a13-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="32a13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32a13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32a13-110">[**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme)結構的指標，此結構會接收色彩配置資訊。</span><span class="sxs-lookup"><span data-stu-id="32a13-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="32a13-111">在傳送此訊息之前，您必須將此結構的 **dwSize** 成員設定為 **sizeof** (COLORSCHEME) 。</span><span class="sxs-lookup"><span data-stu-id="32a13-111">You must set the **dwSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32a13-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="32a13-112">Return value</span></span>

<span data-ttu-id="32a13-113">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="32a13-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="32a13-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="32a13-114">Requirements</span></span>



| <span data-ttu-id="32a13-115">需求</span><span class="sxs-lookup"><span data-stu-id="32a13-115">Requirement</span></span> | <span data-ttu-id="32a13-116">值</span><span class="sxs-lookup"><span data-stu-id="32a13-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32a13-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32a13-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32a13-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32a13-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32a13-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32a13-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32a13-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32a13-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32a13-121">標頭</span><span class="sxs-lookup"><span data-stu-id="32a13-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32a13-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="32a13-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a13-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32a13-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a13-124">**RB \_ SETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="32a13-124">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
</dt> </dl>

 

 





