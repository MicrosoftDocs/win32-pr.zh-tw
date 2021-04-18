---
title: 'TVM_SETAUTOSCROLLINFO 訊息 (Commctrl .h) '
description: 設定用來判斷自動滾動特性的資訊。 您可以使用 TreeView SetAutoScrollInfo 宏明確地傳送此訊息 \_ 。
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967329"
---
# <a name="tvm_setautoscrollinfo-message"></a><span data-ttu-id="8c9ed-105">TVM \_ SETAUTOSCROLLINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="8c9ed-105">TVM\_SETAUTOSCROLLINFO message</span></span>

<span data-ttu-id="8c9ed-106">設定用來判斷自動滾動特性的資訊。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-106">Sets information used to determine auto-scroll characteristics.</span></span> <span data-ttu-id="8c9ed-107">您可以使用 [**TreeView \_ SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-107">You can send this message explicitly or by using the [**TreeView\_SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c9ed-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c9ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c9ed-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c9ed-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c9ed-110">指定每秒的圖元數。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-110">Specifies pixels per second.</span></span> <span data-ttu-id="8c9ed-111">滾動的位移會除以 *wParam* ，以決定自動捲軸的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-111">The offset to scroll is divided by the *wParam* to determine the total duration of the auto-scroll.</span></span>

</dd> <dt>

<span data-ttu-id="8c9ed-112">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c9ed-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c9ed-113">指定重繪時間間隔。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-113">Specifies the redraw time interval.</span></span> <span data-ttu-id="8c9ed-114">在每個 elasped 間隔重繪，直到專案滾動到視野為止。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-114">Redraw at every elasped interval, until the item is scrolled into view.</span></span> <span data-ttu-id="8c9ed-115">指定 *wParam* 時，會計算專案的位置，並進行重新繪製。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-115">Given *wParam*, the location of the item is calculated and a repaint occurs.</span></span> <span data-ttu-id="8c9ed-116">設定此值以建立平滑滾動。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-116">Set this value to create smooth scrolling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c9ed-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c9ed-117">Return value</span></span>

<span data-ttu-id="8c9ed-118">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-118">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c9ed-119">備註</span><span class="sxs-lookup"><span data-stu-id="8c9ed-119">Remarks</span></span>

<span data-ttu-id="8c9ed-120">Autoscroll 資訊可用來將看不見專案滾動到視野中。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-120">Autoscroll information is used to scroll a nonvisible item into view.</span></span> <span data-ttu-id="8c9ed-121">控制項必須有 [**tv \_ EX \_ AUTOHSCROLL**](tree-view-control-window-extended-styles.md) 延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-121">The control must have the [**TVS\_EX\_AUTOHSCROLL**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="8c9ed-122">如需擴充樣式的詳細資訊，請參閱 Tree-View 控制延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-122">For information on extended styles, see Tree-View Control Extended Styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9ed-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c9ed-123">Requirements</span></span>



| <span data-ttu-id="8c9ed-124">需求</span><span class="sxs-lookup"><span data-stu-id="8c9ed-124">Requirement</span></span> | <span data-ttu-id="8c9ed-125">值</span><span class="sxs-lookup"><span data-stu-id="8c9ed-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9ed-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c9ed-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9ed-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c9ed-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c9ed-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c9ed-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9ed-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c9ed-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c9ed-130">標頭</span><span class="sxs-lookup"><span data-stu-id="8c9ed-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9ed-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c9ed-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





