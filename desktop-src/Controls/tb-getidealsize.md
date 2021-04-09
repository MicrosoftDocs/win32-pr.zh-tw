---
title: 'TB_GETIDEALSIZE 訊息 (Commctrl .h) '
description: 取得工具列的理想大小。
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024722"
---
# <a name="tb_getidealsize-message"></a><span data-ttu-id="c06be-104">TB \_ GETIDEALSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="c06be-104">TB\_GETIDEALSIZE message</span></span>

<span data-ttu-id="c06be-105">取得工具列的理想大小。</span><span class="sxs-lookup"><span data-stu-id="c06be-105">Gets the ideal size of the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c06be-106">參數</span><span class="sxs-lookup"><span data-stu-id="c06be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c06be-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c06be-108">**布林** 值，指出是否要取出工具列的理想高度或寬度。</span><span class="sxs-lookup"><span data-stu-id="c06be-108">A **BOOL** that indicates whether to retrieve the ideal height or width of the toolbar.</span></span> <span data-ttu-id="c06be-109">您可以使用 **TRUE** 來取得理想的高度， **FALSE** 以抓取理想的寬度。</span><span class="sxs-lookup"><span data-stu-id="c06be-109">Use **TRUE** to retrieve the ideal height, **FALSE** to retrieve the ideal width.</span></span></dd> <dt>

<span data-ttu-id="c06be-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c06be-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c06be-111">[**大小**](/previous-versions//dd145106(v=vs.85))結構的指標，該結構會接收所有按鈕的顯示高度或寬度。</span><span class="sxs-lookup"><span data-stu-id="c06be-111">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the height or width at which all buttons would be displayed.</span></span> <span data-ttu-id="c06be-112">如果 *wParam* 為 **TRUE**，則只有 **cy** 成員 (height) 有效。</span><span class="sxs-lookup"><span data-stu-id="c06be-112">If *wParam* is **TRUE**, only the **cy** member (height) is valid.</span></span> <span data-ttu-id="c06be-113">如果 *wParam* 為 **FALSE**，則只有 **cx** 成員 (寬度) 有效。</span><span class="sxs-lookup"><span data-stu-id="c06be-113">If *wParam* is **FALSE**, only the **cx** member (width) is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c06be-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c06be-114">Return value</span></span>

<span data-ttu-id="c06be-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c06be-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c06be-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c06be-116">Requirements</span></span>



| <span data-ttu-id="c06be-117">需求</span><span class="sxs-lookup"><span data-stu-id="c06be-117">Requirement</span></span> | <span data-ttu-id="c06be-118">值</span><span class="sxs-lookup"><span data-stu-id="c06be-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c06be-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c06be-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c06be-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c06be-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c06be-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c06be-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c06be-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c06be-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c06be-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c06be-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c06be-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c06be-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

