---
title: 'LVM_GETINSERTMARK 訊息 (Commctrl .h) '
description: 抓取插入點的位置。
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- LVM_GETINSERTMARK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843352"
---
# <a name="lvm_getinsertmark-message"></a><span data-ttu-id="9df04-104">LVM \_ GETINSERTMARK 訊息</span><span class="sxs-lookup"><span data-stu-id="9df04-104">LVM\_GETINSERTMARK message</span></span>

<span data-ttu-id="9df04-105">抓取插入點的位置。</span><span class="sxs-lookup"><span data-stu-id="9df04-105">Retrieves the position of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="9df04-106">參數</span><span class="sxs-lookup"><span data-stu-id="9df04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9df04-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9df04-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9df04-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9df04-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9df04-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9df04-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9df04-110"><a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a>結構的指標，此結構會接收插入點的位置。</span><span class="sxs-lookup"><span data-stu-id="9df04-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that receives the position of the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9df04-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9df04-111">Return value</span></span>

<span data-ttu-id="9df04-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9df04-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="9df04-113">如果 [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark)結構之 **cbSize** 成員中的大小不等於結構的實際大小，就會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9df04-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9df04-114">備註</span><span class="sxs-lookup"><span data-stu-id="9df04-114">Remarks</span></span>

<span data-ttu-id="9df04-115">只有在清單視圖控制項處於圖示視圖、小型圖示視圖或磚視圖，而且不在群組視圖模式中時，才會出現插入點。</span><span class="sxs-lookup"><span data-stu-id="9df04-115">An insertion point can appear only if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="9df04-116">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="9df04-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9df04-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="9df04-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9df04-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9df04-118">Requirements</span></span>



| <span data-ttu-id="9df04-119">需求</span><span class="sxs-lookup"><span data-stu-id="9df04-119">Requirement</span></span> | <span data-ttu-id="9df04-120">值</span><span class="sxs-lookup"><span data-stu-id="9df04-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9df04-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9df04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9df04-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9df04-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9df04-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9df04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9df04-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9df04-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9df04-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9df04-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9df04-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9df04-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





