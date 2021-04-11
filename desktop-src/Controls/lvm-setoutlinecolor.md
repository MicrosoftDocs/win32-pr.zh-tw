---
title: 'LVM_SETOUTLINECOLOR 訊息 (Commctrl .h) '
description: 如果 \_ \_ 已設定 lvs) EX BORDERSELECT 擴充視窗樣式，則設定清單視圖控制項框線的色彩。
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843091"
---
# <a name="lvm_setoutlinecolor-message"></a><span data-ttu-id="e302e-104">LVM \_ SETOUTLINECOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="e302e-104">LVM\_SETOUTLINECOLOR message</span></span>

<span data-ttu-id="e302e-105">如果已設定 [**lvs) \_ EX \_ BORDERSELECT**](extended-list-view-styles.md) 擴充視窗樣式，則設定清單視圖控制項框線的色彩。</span><span class="sxs-lookup"><span data-stu-id="e302e-105">Sets the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="e302e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e302e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e302e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e302e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e302e-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e302e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e302e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e302e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e302e-110">**COLORREF** 結構，指定要設定框線的色彩。</span><span class="sxs-lookup"><span data-stu-id="e302e-110">**COLORREF** structure that specifies the color to set the border.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e302e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e302e-111">Return value</span></span>

<span data-ttu-id="e302e-112">傳回包含外框色彩的 **COLORREF** 結構。</span><span class="sxs-lookup"><span data-stu-id="e302e-112">Returns **COLORREF** structure that contains the outline color.</span></span>

## <a name="remarks"></a><span data-ttu-id="e302e-113">備註</span><span class="sxs-lookup"><span data-stu-id="e302e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e302e-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="e302e-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e302e-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="e302e-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e302e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e302e-116">Requirements</span></span>



| <span data-ttu-id="e302e-117">需求</span><span class="sxs-lookup"><span data-stu-id="e302e-117">Requirement</span></span> | <span data-ttu-id="e302e-118">值</span><span class="sxs-lookup"><span data-stu-id="e302e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e302e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e302e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e302e-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e302e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e302e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e302e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e302e-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e302e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e302e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e302e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e302e-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e302e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





