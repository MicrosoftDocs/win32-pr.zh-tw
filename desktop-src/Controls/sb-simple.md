---
title: 'SB_SIMPLE 訊息 (Commctrl .h) '
description: 指定狀態視窗是否顯示簡單文字，或顯示先前 SB SETPARTS 訊息所設定的所有視窗元件 \_ 。
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105065"
---
# <a name="sb_simple-message"></a><span data-ttu-id="4a863-104">SB \_ 簡單訊息</span><span class="sxs-lookup"><span data-stu-id="4a863-104">SB\_SIMPLE message</span></span>

<span data-ttu-id="4a863-105">指定狀態視窗是否顯示簡單文字，或顯示先前 [**SB \_ SETPARTS**](sb-setparts.md) 訊息所設定的所有視窗元件。</span><span class="sxs-lookup"><span data-stu-id="4a863-105">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a863-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a863-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a863-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a863-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a863-108">顯示類型旗標。</span><span class="sxs-lookup"><span data-stu-id="4a863-108">Display type flag.</span></span> <span data-ttu-id="4a863-109">如果此參數為 **TRUE**，視窗會顯示簡單文字。</span><span class="sxs-lookup"><span data-stu-id="4a863-109">If this parameter is **TRUE**, the window displays simple text.</span></span> <span data-ttu-id="4a863-110">如果為 **FALSE**，則會顯示多個部分。</span><span class="sxs-lookup"><span data-stu-id="4a863-110">If it is **FALSE**, it displays multiple parts.</span></span>

</dd> <dt>

<span data-ttu-id="4a863-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a863-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4a863-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4a863-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a863-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a863-113">Return value</span></span>

<span data-ttu-id="4a863-114">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="4a863-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a863-115">備註</span><span class="sxs-lookup"><span data-stu-id="4a863-115">Remarks</span></span>

<span data-ttu-id="4a863-116">如果狀態視窗是從簡單變更為 simple，或反之亦然，則會立即重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="4a863-116">If the status window is being changed from nonsimple to simple, or vice versa, the window is immediately redrawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a863-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a863-117">Requirements</span></span>



| <span data-ttu-id="4a863-118">需求</span><span class="sxs-lookup"><span data-stu-id="4a863-118">Requirement</span></span> | <span data-ttu-id="4a863-119">值</span><span class="sxs-lookup"><span data-stu-id="4a863-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a863-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a863-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a863-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a863-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a863-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a863-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a863-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a863-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a863-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4a863-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a863-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a863-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





