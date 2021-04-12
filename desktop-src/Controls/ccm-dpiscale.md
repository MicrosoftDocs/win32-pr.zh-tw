---
title: 'CCM_DPISCALE 訊息 (Commctrl .h) '
description: 在 Tree-View 控制項、List-View 控制項、ComboBoxEx 控制項、標題控制項、按鈕、工具列控制項、動畫控制項和影像清單中，啟用每英寸的自動大點 (DPI) 縮放比例。
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE message Windows 控制項
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104519"
---
# <a name="ccm_dpiscale-message"></a><span data-ttu-id="4adbc-104">CCM \_ DPISCALE 訊息</span><span class="sxs-lookup"><span data-stu-id="4adbc-104">CCM\_DPISCALE message</span></span>

<span data-ttu-id="4adbc-105">在 [樹狀檢視控制項](tree-view-controls.md)、 [清單視圖控制項](list-view-control-reference.md)、 [ComboBoxEx 控制項](comboboxex-controls.md)、 [標題控制項](header-controls.md)、 [按鈕](buttons.md)、 [工具列控制項](toolbar-controls-overview.md)、 [動畫控制項](animation-control-overview.md)和 [影像清單](image-lists.md)中，啟用每英寸的自動大點 (DPI) 縮放比例。</span><span class="sxs-lookup"><span data-stu-id="4adbc-105">Enables automatic high dots per inch (dpi) scaling in [Tree-View controls](tree-view-controls.md), [List-View controls](list-view-control-reference.md), [ComboBoxEx controls](comboboxex-controls.md), [Header controls](header-controls.md), [Buttons](buttons.md), [Toolbar controls](toolbar-controls-overview.md), [Animation controls](animation-control-overview.md), and [Image Lists](image-lists.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="4adbc-106">參數</span><span class="sxs-lookup"><span data-stu-id="4adbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4adbc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4adbc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4adbc-108">設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4adbc-108">Set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4adbc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4adbc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4adbc-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4adbc-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4adbc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4adbc-111">Return value</span></span>

<span data-ttu-id="4adbc-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="4adbc-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4adbc-113">備註</span><span class="sxs-lookup"><span data-stu-id="4adbc-113">Remarks</span></span>

<span data-ttu-id="4adbc-114">快速啟動和 [工作列](/windows/desktop/shell/taskbar) 不應指定 DPI 縮放比例，因為影像已經過調整。</span><span class="sxs-lookup"><span data-stu-id="4adbc-114">Quick Launch and [Taskbar](/windows/desktop/shell/taskbar) should not specify a dpi scaling, because the images are already scaled.</span></span>

<span data-ttu-id="4adbc-115">任何使用以 SmallIcon 度量建立之影像清單的控制項，都不應該調整其圖示。</span><span class="sxs-lookup"><span data-stu-id="4adbc-115">Any control that uses an image list created with the SmallIcon metric should not scale its icons.</span></span>

> [!Note]  
> <span data-ttu-id="4adbc-116">若要使用此 API，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="4adbc-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4adbc-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4adbc-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4adbc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4adbc-118">Requirements</span></span>



| <span data-ttu-id="4adbc-119">需求</span><span class="sxs-lookup"><span data-stu-id="4adbc-119">Requirement</span></span> | <span data-ttu-id="4adbc-120">值</span><span class="sxs-lookup"><span data-stu-id="4adbc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4adbc-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4adbc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4adbc-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4adbc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4adbc-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4adbc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4adbc-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4adbc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4adbc-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4adbc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4adbc-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4adbc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

