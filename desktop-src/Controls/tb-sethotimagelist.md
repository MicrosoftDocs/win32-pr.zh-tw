---
title: 'TB_SETHOTIMAGELIST 訊息 (Commctrl .h) '
description: 設定工具列控制項將用來顯示熱按鈕的影像清單。
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934784"
---
# <a name="tb_sethotimagelist-message"></a><span data-ttu-id="0a226-104">TB \_ SETHOTIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="0a226-104">TB\_SETHOTIMAGELIST message</span></span>

<span data-ttu-id="0a226-105">設定工具列控制項將用來顯示熱按鈕的影像清單。</span><span class="sxs-lookup"><span data-stu-id="0a226-105">Sets the image list that the toolbar control will use to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a226-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a226-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a226-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a226-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0a226-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0a226-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0a226-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a226-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a226-110">將設定之影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0a226-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a226-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a226-111">Return value</span></span>

<span data-ttu-id="0a226-112">傳回先前用來顯示熱按鈕的影像清單控制碼，如果先前未設定任何影像清單，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0a226-112">Returns the handle to the image list previously used to display hot buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a226-113">備註</span><span class="sxs-lookup"><span data-stu-id="0a226-113">Remarks</span></span>

<span data-ttu-id="0a226-114">當游標停留在按鈕上時，按鈕會是經常性的。</span><span class="sxs-lookup"><span data-stu-id="0a226-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="0a226-115">Toolbar 控制項必須具有 [**TBSTYLE 的 \_**](toolbar-control-and-button-styles.md) 一般或 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式，才能有熱專案。</span><span class="sxs-lookup"><span data-stu-id="0a226-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a226-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a226-116">Requirements</span></span>



| <span data-ttu-id="0a226-117">需求</span><span class="sxs-lookup"><span data-stu-id="0a226-117">Requirement</span></span> | <span data-ttu-id="0a226-118">值</span><span class="sxs-lookup"><span data-stu-id="0a226-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a226-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a226-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a226-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a226-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a226-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a226-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a226-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a226-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a226-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0a226-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a226-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a226-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





