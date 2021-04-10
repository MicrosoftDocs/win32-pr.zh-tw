---
title: 'LVM_GETTILEINFO 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項中的圖格相關資訊。
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- LVM_GETTILEINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025375"
---
# <a name="lvm_gettileinfo-message"></a><span data-ttu-id="f95b3-104">LVM \_ GETTILEINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="f95b3-104">LVM\_GETTILEINFO message</span></span>

<span data-ttu-id="f95b3-105">抓取清單視圖控制項中的圖格相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f95b3-105">Retrieves information about a tile in a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f95b3-106">參數</span><span class="sxs-lookup"><span data-stu-id="f95b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f95b3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f95b3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f95b3-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f95b3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f95b3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f95b3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f95b3-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a>結構的指標，此結構會接收抓取的資訊。</span><span class="sxs-lookup"><span data-stu-id="f95b3-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f95b3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f95b3-111">Return value</span></span>

<span data-ttu-id="f95b3-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="f95b3-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f95b3-113">備註</span><span class="sxs-lookup"><span data-stu-id="f95b3-113">Remarks</span></span>

<span data-ttu-id="f95b3-114">磚視圖是在清單視圖控制項中排列和顯示專案的新方式。</span><span class="sxs-lookup"><span data-stu-id="f95b3-114">Tile view is a new way of arranging and displaying items in a list-view control.</span></span> <span data-ttu-id="f95b3-115">其他的視圖是圖示、小型圖示、詳細資料和清單。</span><span class="sxs-lookup"><span data-stu-id="f95b3-115">The other views are icon, small icon, details, and list.</span></span>

> [!Note]  
> <span data-ttu-id="f95b3-116">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="f95b3-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f95b3-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f95b3-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f95b3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f95b3-118">Requirements</span></span>



| <span data-ttu-id="f95b3-119">需求</span><span class="sxs-lookup"><span data-stu-id="f95b3-119">Requirement</span></span> | <span data-ttu-id="f95b3-120">值</span><span class="sxs-lookup"><span data-stu-id="f95b3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f95b3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f95b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f95b3-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f95b3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f95b3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f95b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f95b3-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f95b3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f95b3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f95b3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f95b3-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f95b3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





