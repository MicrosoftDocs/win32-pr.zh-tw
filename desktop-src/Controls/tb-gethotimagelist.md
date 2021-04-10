---
title: 'TB_GETHOTIMAGELIST 訊息 (Commctrl .h) '
description: 抓取工具列控制項用來顯示熱按鈕的影像清單。
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104028"
---
# <a name="tb_gethotimagelist-message"></a><span data-ttu-id="25718-104">TB \_ GETHOTIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="25718-104">TB\_GETHOTIMAGELIST message</span></span>

<span data-ttu-id="25718-105">抓取工具列控制項用來顯示熱按鈕的影像清單。</span><span class="sxs-lookup"><span data-stu-id="25718-105">Retrieves the image list that a toolbar control uses to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="25718-106">參數</span><span class="sxs-lookup"><span data-stu-id="25718-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25718-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25718-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25718-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="25718-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25718-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25718-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="25718-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="25718-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25718-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="25718-111">Return value</span></span>

<span data-ttu-id="25718-112">傳回影像清單的控制碼，控制項會使用此控制碼來顯示熱按鈕; 如果未設定任何熱影像清單，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="25718-112">Returns the handle to the image list that the control uses to display hot buttons, or **NULL** if no hot image list is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="25718-113">備註</span><span class="sxs-lookup"><span data-stu-id="25718-113">Remarks</span></span>

<span data-ttu-id="25718-114">當游標停留在按鈕上時，按鈕會是經常性的。</span><span class="sxs-lookup"><span data-stu-id="25718-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="25718-115">Toolbar 控制項必須具有 [**TBSTYLE 的 \_**](toolbar-control-and-button-styles.md) 一般或 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式，才能有熱專案。</span><span class="sxs-lookup"><span data-stu-id="25718-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="25718-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="25718-116">Requirements</span></span>



| <span data-ttu-id="25718-117">需求</span><span class="sxs-lookup"><span data-stu-id="25718-117">Requirement</span></span> | <span data-ttu-id="25718-118">值</span><span class="sxs-lookup"><span data-stu-id="25718-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25718-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25718-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25718-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25718-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25718-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25718-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25718-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25718-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25718-123">標頭</span><span class="sxs-lookup"><span data-stu-id="25718-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="25718-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="25718-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





