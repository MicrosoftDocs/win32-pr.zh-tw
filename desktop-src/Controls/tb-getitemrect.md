---
title: 'TB_GETITEMRECT 訊息 (Commctrl .h) '
description: 抓取工具列中按鈕的周框。
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843991"
---
# <a name="tb_getitemrect-message"></a><span data-ttu-id="9596c-104">TB \_ GETITEMRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="9596c-104">TB\_GETITEMRECT message</span></span>

<span data-ttu-id="9596c-105">抓取工具列中按鈕的周框。</span><span class="sxs-lookup"><span data-stu-id="9596c-105">Retrieves the bounding rectangle of a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9596c-106">參數</span><span class="sxs-lookup"><span data-stu-id="9596c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9596c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9596c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9596c-108">以零為基底的按鈕索引，用來取得資訊。</span><span class="sxs-lookup"><span data-stu-id="9596c-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="9596c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9596c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9596c-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收周框矩形的用戶端座標。</span><span class="sxs-lookup"><span data-stu-id="9596c-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the client coordinates of the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9596c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9596c-111">Return value</span></span>

<span data-ttu-id="9596c-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9596c-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9596c-113">備註</span><span class="sxs-lookup"><span data-stu-id="9596c-113">Remarks</span></span>

<span data-ttu-id="9596c-114">此訊息不會針對其狀態設定為 [**TBSTATE \_ 隱藏**](toolbar-button-states.md) 值的按鈕，取得周框矩形。</span><span class="sxs-lookup"><span data-stu-id="9596c-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9596c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9596c-115">Requirements</span></span>



| <span data-ttu-id="9596c-116">需求</span><span class="sxs-lookup"><span data-stu-id="9596c-116">Requirement</span></span> | <span data-ttu-id="9596c-117">值</span><span class="sxs-lookup"><span data-stu-id="9596c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9596c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9596c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9596c-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9596c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9596c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9596c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9596c-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9596c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9596c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9596c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9596c-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9596c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

