---
title: 'LVM_SETINSERTMARK 訊息 (Commctrl .h) '
description: 將插入點設定為已定義的位置。
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- LVM_SETINSERTMARK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093832"
---
# <a name="lvm_setinsertmark-message"></a><span data-ttu-id="1134d-104">LVM \_ SETINSERTMARK 訊息</span><span class="sxs-lookup"><span data-stu-id="1134d-104">LVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="1134d-105">將插入點設定為已定義的位置。</span><span class="sxs-lookup"><span data-stu-id="1134d-105">Sets the insertion point to the defined position.</span></span>

## <a name="parameters"></a><span data-ttu-id="1134d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1134d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1134d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1134d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1134d-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1134d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1134d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1134d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1134d-110"><a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a>結構的指標，指定要設定插入點的位置。</span><span class="sxs-lookup"><span data-stu-id="1134d-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies where to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1134d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1134d-111">Return value</span></span>

<span data-ttu-id="1134d-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1134d-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="1134d-113">如果 [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark)結構之 **cbSize** 成員中的大小不等於結構的實際大小，或當插入點不適用於目前的視圖時，則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1134d-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="1134d-114">備註</span><span class="sxs-lookup"><span data-stu-id="1134d-114">Remarks</span></span>

<span data-ttu-id="1134d-115">只有在清單視圖控制項處於圖示視圖、小型圖示視圖或磚視圖，而且不在群組視圖模式中時，才會出現插入點。</span><span class="sxs-lookup"><span data-stu-id="1134d-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="1134d-116">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="1134d-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1134d-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1134d-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1134d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1134d-118">Requirements</span></span>



| <span data-ttu-id="1134d-119">需求</span><span class="sxs-lookup"><span data-stu-id="1134d-119">Requirement</span></span> | <span data-ttu-id="1134d-120">值</span><span class="sxs-lookup"><span data-stu-id="1134d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1134d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1134d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1134d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1134d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1134d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1134d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1134d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1134d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1134d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1134d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1134d-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1134d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





