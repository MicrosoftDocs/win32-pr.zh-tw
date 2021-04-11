---
title: 'LVM_INSERTMARKHITTEST 訊息 (Commctrl .h) '
description: 抓取最接近指定點的插入點。
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105479"
---
# <a name="lvm_insertmarkhittest-message"></a><span data-ttu-id="ce53e-104">LVM \_ INSERTMARKHITTEST 訊息</span><span class="sxs-lookup"><span data-stu-id="ce53e-104">LVM\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="ce53e-105">抓取最接近指定點的插入點。</span><span class="sxs-lookup"><span data-stu-id="ce53e-105">Retrieves the insertion point closest to a specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce53e-106">參數</span><span class="sxs-lookup"><span data-stu-id="ce53e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce53e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce53e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce53e-108">指向包含點擊測試座標之 **點** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ce53e-108">Pointer to a **POINT** structure that contains the hit test coordinates.</span></span></dd> <dt>

<span data-ttu-id="ce53e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce53e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ce53e-110"><a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a>結構的指標，指定最接近 *wParam* 參數所定義之座標的插入點。</span><span class="sxs-lookup"><span data-stu-id="ce53e-110">Pointer to an <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies the insertion point closest to the coordinates defined by the *wParam* parameter.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce53e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce53e-111">Return value</span></span>

<span data-ttu-id="ce53e-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ce53e-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="ce53e-113">如果 [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark)結構之 **cbSize** 成員中的大小不等於結構的實際大小，或當插入點不適用於目前的視圖時，則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ce53e-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce53e-114">備註</span><span class="sxs-lookup"><span data-stu-id="ce53e-114">Remarks</span></span>

<span data-ttu-id="ce53e-115">只有當清單視圖控制項處於圖示視圖、小型圖示視圖或磚視圖，而且不在群組視圖模式中時，才會出現插入點。</span><span class="sxs-lookup"><span data-stu-id="ce53e-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view and is not in group-view mode.</span></span>

<span data-ttu-id="ce53e-116">如果不適用此視圖的插入點， [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) 結構會在 **iItem** 成員中包含-1。</span><span class="sxs-lookup"><span data-stu-id="ce53e-116">If insertion points do not apply for the view, the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure contains a -1 in the **iItem** member.</span></span>

> [!Note]  
> <span data-ttu-id="ce53e-117">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="ce53e-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ce53e-118">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="ce53e-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce53e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce53e-119">Requirements</span></span>



| <span data-ttu-id="ce53e-120">需求</span><span class="sxs-lookup"><span data-stu-id="ce53e-120">Requirement</span></span> | <span data-ttu-id="ce53e-121">值</span><span class="sxs-lookup"><span data-stu-id="ce53e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce53e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce53e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce53e-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce53e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce53e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce53e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce53e-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce53e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce53e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ce53e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce53e-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce53e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





