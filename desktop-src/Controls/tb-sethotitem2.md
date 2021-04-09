---
title: 'TB_SETHOTITEM2 訊息 (Commctrl .h) '
description: 設定工具列中的熱專案。
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686195"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="0a7d9-104">TB \_ SETHOTITEM2 訊息</span><span class="sxs-lookup"><span data-stu-id="0a7d9-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="0a7d9-105">設定工具列中的熱專案。</span><span class="sxs-lookup"><span data-stu-id="0a7d9-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a7d9-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a7d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a7d9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a7d9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a7d9-108">將設為經常性存取之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="0a7d9-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="0a7d9-109">如果這個值是-1，則沒有任何專案會是經常性的。</span><span class="sxs-lookup"><span data-stu-id="0a7d9-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="0a7d9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a7d9-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0a7d9-111">HICF \_ xxx 旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="0a7d9-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="0a7d9-112">請參閱 <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>。</span><span class="sxs-lookup"><span data-stu-id="0a7d9-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a7d9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a7d9-113">Return value</span></span>

<span data-ttu-id="0a7d9-114">傳回先前熱專案的索引，如果沒有熱專案，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="0a7d9-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a7d9-115">備註</span><span class="sxs-lookup"><span data-stu-id="0a7d9-115">Remarks</span></span>

<span data-ttu-id="0a7d9-116">未針對沒有 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式的工具列定義此訊息的行為。</span><span class="sxs-lookup"><span data-stu-id="0a7d9-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a7d9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a7d9-117">Requirements</span></span>



| <span data-ttu-id="0a7d9-118">需求</span><span class="sxs-lookup"><span data-stu-id="0a7d9-118">Requirement</span></span> | <span data-ttu-id="0a7d9-119">值</span><span class="sxs-lookup"><span data-stu-id="0a7d9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7d9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a7d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0a7d9-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a7d9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a7d9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a7d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0a7d9-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a7d9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a7d9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0a7d9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a7d9-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





