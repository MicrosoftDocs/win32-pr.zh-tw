---
title: 'HDM_SETHOTDIVIDER 訊息 (Commctrl .h) '
description: 變更標題專案之間的分隔線色彩，以表示外部拖放作業的目的地。 您可以明確地傳送此訊息，或使用標頭 \_ SetHotDivider 宏。
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094500"
---
# <a name="hdm_sethotdivider-message"></a><span data-ttu-id="d41ae-105">HDM \_ SETHOTDIVIDER 訊息</span><span class="sxs-lookup"><span data-stu-id="d41ae-105">HDM\_SETHOTDIVIDER message</span></span>

<span data-ttu-id="d41ae-106">變更標題專案之間的分隔線色彩，以表示外部拖放作業的目的地。</span><span class="sxs-lookup"><span data-stu-id="d41ae-106">Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation.</span></span> <span data-ttu-id="d41ae-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) 宏。</span><span class="sxs-lookup"><span data-stu-id="d41ae-107">You can send this message explicitly or use the [**Header\_SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d41ae-108">參數</span><span class="sxs-lookup"><span data-stu-id="d41ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41ae-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d41ae-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d41ae-110">*LParam* 所代表的數值型別。</span><span class="sxs-lookup"><span data-stu-id="d41ae-110">The type of value represented by *lParam*.</span></span> <span data-ttu-id="d41ae-111">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="d41ae-111">This value can be one of the following:</span></span>



| <span data-ttu-id="d41ae-112">值</span><span class="sxs-lookup"><span data-stu-id="d41ae-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="d41ae-113">意義</span><span class="sxs-lookup"><span data-stu-id="d41ae-113">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="d41ae-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d41ae-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="d41ae-115">表示 *lParam* 保存指標的用戶端座標。</span><span class="sxs-lookup"><span data-stu-id="d41ae-115">Indicates that *lParam* holds the client coordinates of the pointer.</span></span><br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="d41ae-116"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d41ae-116"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="d41ae-117">表示 *lParam* 保留分割索引值。</span><span class="sxs-lookup"><span data-stu-id="d41ae-117">Indicates that *lParam* holds a divider index value.</span></span><br/>                 |



 

</dd> <dt>

<span data-ttu-id="d41ae-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d41ae-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d41ae-119">*LParam* 中保留的值會根據 *wParam* 的值來解讀。</span><span class="sxs-lookup"><span data-stu-id="d41ae-119">A value held in *lParam* is interpreted depending on the value of *wParam*.</span></span>

<span data-ttu-id="d41ae-120">如果 *wParam* 為 **TRUE**，則 *lParam* 代表指標的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="d41ae-120">If *wParam* is **TRUE**, *lParam* represents the x- and y-coordinates of the pointer.</span></span> <span data-ttu-id="d41ae-121">X 座標是在低字組中，而 y 座標則是在高字中。</span><span class="sxs-lookup"><span data-stu-id="d41ae-121">The x-coordinate is in the low word, and the y-coordinate is in the high word.</span></span> <span data-ttu-id="d41ae-122">當標題控制項接收訊息時，它會根據 *lParam* 座標反白顯示適當的分隔線。</span><span class="sxs-lookup"><span data-stu-id="d41ae-122">When the header control receives the message, it highlights the appropriate divider based on the *lParam* coordinates.</span></span>

<span data-ttu-id="d41ae-123">如果 *wParam* 為 **FALSE**，則 *lParam* 代表要反白顯示之分隔線的整數索引。</span><span class="sxs-lookup"><span data-stu-id="d41ae-123">If *wParam* is **FALSE**, *lParam* represents the integer index of the divider to be highlighted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d41ae-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="d41ae-124">Return value</span></span>

<span data-ttu-id="d41ae-125">傳回等於控制項反白顯示之分隔線索引的值。</span><span class="sxs-lookup"><span data-stu-id="d41ae-125">Returns a value equal to the index of the divider that the control highlighted.</span></span>

## <a name="remarks"></a><span data-ttu-id="d41ae-126">備註</span><span class="sxs-lookup"><span data-stu-id="d41ae-126">Remarks</span></span>

<span data-ttu-id="d41ae-127">當標題控制項具有 [**HDS \_ system.windows.dragdrop.drop>**](header-control-styles.md) 樣式時，此訊息會產生一個效果。</span><span class="sxs-lookup"><span data-stu-id="d41ae-127">This message creates an effect that a header control automatically produces when it has the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="d41ae-128">當控制項的擁有者以手動方式處理拖放作業時，會使用 **HDM \_ SETHOTDIVIDER** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d41ae-128">The **HDM\_SETHOTDIVIDER** message is intended to be used when the owner of the control handles drag-and-drop operations manually.</span></span>

## <a name="requirements"></a><span data-ttu-id="d41ae-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d41ae-129">Requirements</span></span>



| <span data-ttu-id="d41ae-130">需求</span><span class="sxs-lookup"><span data-stu-id="d41ae-130">Requirement</span></span> | <span data-ttu-id="d41ae-131">值</span><span class="sxs-lookup"><span data-stu-id="d41ae-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d41ae-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d41ae-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d41ae-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d41ae-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d41ae-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d41ae-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d41ae-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d41ae-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d41ae-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d41ae-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d41ae-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d41ae-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





