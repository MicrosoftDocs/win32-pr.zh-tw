---
title: 'TB_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 設定工具列控制項的延伸樣式。
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- TB_SETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105041"
---
# <a name="tb_setextendedstyle-message"></a><span data-ttu-id="e8e95-104">TB \_ SETEXTENDEDSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="e8e95-104">TB\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="e8e95-105">設定工具列控制項的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="e8e95-105">Sets the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8e95-106">參數</span><span class="sxs-lookup"><span data-stu-id="e8e95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e95-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8e95-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8e95-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e8e95-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e8e95-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8e95-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e95-110">指定新擴充樣式的值。</span><span class="sxs-lookup"><span data-stu-id="e8e95-110">Value specifying the new extended styles.</span></span> <span data-ttu-id="e8e95-111">這個參數可以是 [擴充樣式](toolbar-extended-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="e8e95-111">This parameter can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e95-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8e95-112">Return value</span></span>

<span data-ttu-id="e8e95-113">傳回表示先前擴充樣式的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="e8e95-113">Returns a **DWORD** that represents the previous extended styles.</span></span> <span data-ttu-id="e8e95-114">這個值可以是 [擴充樣式](toolbar-extended-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="e8e95-114">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e95-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8e95-115">Requirements</span></span>



| <span data-ttu-id="e8e95-116">需求</span><span class="sxs-lookup"><span data-stu-id="e8e95-116">Requirement</span></span> | <span data-ttu-id="e8e95-117">值</span><span class="sxs-lookup"><span data-stu-id="e8e95-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e95-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8e95-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e95-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8e95-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8e95-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8e95-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e95-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8e95-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8e95-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e8e95-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e95-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e95-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e95-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8e95-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e95-125">**TB \_ GETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="e8e95-125">**TB\_GETEXTENDEDSTYLE**</span></span>](tb-getextendedstyle.md)
</dt> </dl>

 

 





