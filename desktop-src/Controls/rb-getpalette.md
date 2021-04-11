---
title: 'RB_GETPALETTE 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項的目前調色板。
ms.assetid: f9eeefb3-8308-45bf-89e4-4f282ee6d935
keywords:
- RB_GETPALETTE message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36dd2764b6a8951a337c990dcbcfb8e5aff9c56b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104447"
---
# <a name="rb_getpalette-message"></a><span data-ttu-id="d61db-104">RB \_ GETPALETTE 訊息</span><span class="sxs-lookup"><span data-stu-id="d61db-104">RB\_GETPALETTE message</span></span>

<span data-ttu-id="d61db-105">抓取 Rebar 控制項的目前調色板。</span><span class="sxs-lookup"><span data-stu-id="d61db-105">Retrieves the rebar control's current palette.</span></span>

## <a name="parameters"></a><span data-ttu-id="d61db-106">參數</span><span class="sxs-lookup"><span data-stu-id="d61db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d61db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d61db-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d61db-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d61db-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d61db-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d61db-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d61db-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d61db-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d61db-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d61db-111">Return value</span></span>

<span data-ttu-id="d61db-112">傳回 **HPALETTE** ，指定 Rebar 控制項目前的調色板。</span><span class="sxs-lookup"><span data-stu-id="d61db-112">Returns an **HPALETTE** that specifies the rebar control's current palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="d61db-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d61db-113">Requirements</span></span>



| <span data-ttu-id="d61db-114">需求</span><span class="sxs-lookup"><span data-stu-id="d61db-114">Requirement</span></span> | <span data-ttu-id="d61db-115">值</span><span class="sxs-lookup"><span data-stu-id="d61db-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d61db-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d61db-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d61db-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d61db-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d61db-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d61db-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d61db-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d61db-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d61db-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d61db-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d61db-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d61db-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d61db-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d61db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d61db-123">**RB \_ SETPALETTE**</span><span class="sxs-lookup"><span data-stu-id="d61db-123">**RB\_SETPALETTE**</span></span>](rb-setpalette.md)
</dt> </dl>

 

 





