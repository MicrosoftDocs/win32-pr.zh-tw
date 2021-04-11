---
title: 'RB_GETROWHEIGHT 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項中指定之資料列的高度。
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843884"
---
# <a name="rb_getrowheight-message"></a><span data-ttu-id="5c865-104">RB \_ GETROWHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="5c865-104">RB\_GETROWHEIGHT message</span></span>

<span data-ttu-id="5c865-105">抓取 Rebar 控制項中指定之資料列的高度。</span><span class="sxs-lookup"><span data-stu-id="5c865-105">Retrieves the height of a specified row in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c865-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c865-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c865-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c865-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c865-108">以零為基底的帶索引。</span><span class="sxs-lookup"><span data-stu-id="5c865-108">Zero-based index of a band.</span></span> <span data-ttu-id="5c865-109">將會取出包含指定之頻外的資料列高度。</span><span class="sxs-lookup"><span data-stu-id="5c865-109">The height of the row that contains the specified band will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="5c865-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c865-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5c865-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5c865-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c865-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c865-112">Return value</span></span>

<span data-ttu-id="5c865-113">傳回代表資料列高度的 **UINT** 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c865-113">Returns a **UINT** value that represents the row height, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c865-114">備註</span><span class="sxs-lookup"><span data-stu-id="5c865-114">Remarks</span></span>

<span data-ttu-id="5c865-115">若要取出 Rebar 控制項中的資料列數目，請使用 [**RB \_ GETROWCOUNT**](rb-getrowcount.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="5c865-115">To retrieve the number of rows in a rebar control, use the [**RB\_GETROWCOUNT**](rb-getrowcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c865-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c865-116">Requirements</span></span>



| <span data-ttu-id="5c865-117">需求</span><span class="sxs-lookup"><span data-stu-id="5c865-117">Requirement</span></span> | <span data-ttu-id="5c865-118">值</span><span class="sxs-lookup"><span data-stu-id="5c865-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c865-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c865-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c865-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c865-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c865-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c865-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c865-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c865-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c865-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5c865-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c865-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c865-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





