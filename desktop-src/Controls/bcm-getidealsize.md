---
title: 'BCM_GETIDEALSIZE 訊息 (Commctrl .h) '
description: 取得最適合其文字和影像的按鈕大小（如果有影像清單）。 您可以明確地傳送此訊息，或使用按鈕 \_ GetIdealSize 宏。
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- BCM_GETIDEALSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965715"
---
# <a name="bcm_getidealsize-message"></a><span data-ttu-id="67f1b-105">BCM \_ GETIDEALSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="67f1b-105">BCM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="67f1b-106">取得最適合其文字和影像的按鈕大小（如果有影像清單）。</span><span class="sxs-lookup"><span data-stu-id="67f1b-106">Gets the size of the button that best fits its text and image, if an image list is present.</span></span> <span data-ttu-id="67f1b-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) 宏。</span><span class="sxs-lookup"><span data-stu-id="67f1b-107">You can send this message explicitly or use the [**Button\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="67f1b-108">參數</span><span class="sxs-lookup"><span data-stu-id="67f1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67f1b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67f1b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67f1b-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="67f1b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67f1b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67f1b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67f1b-112">[**大小**](/previous-versions//dd145106(v=vs.85))結構的指標，該結構會接收所需的按鈕大小，包括文字和影像清單（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="67f1b-112">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the desired size of the button, including text and image list, if present.</span></span> <span data-ttu-id="67f1b-113">呼叫應用程式負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="67f1b-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="67f1b-114">將 **cx** 和 **cy** 成員設定為零，以在 **大小** 結構中傳回理想的高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="67f1b-114">Set the **cx** and **cy** members to zero to have the ideal height and width returned in the **SIZE** structure.</span></span> <span data-ttu-id="67f1b-115">若要指定按鈕寬度，請將 **cx** 成員設定為所需的按鈕寬度。</span><span class="sxs-lookup"><span data-stu-id="67f1b-115">To specify a button width, set the **cx** member to the desired button width.</span></span> <span data-ttu-id="67f1b-116">系統會計算此寬度的理想高度，並將其傳回至 **cy** 成員。</span><span class="sxs-lookup"><span data-stu-id="67f1b-116">The system will calculate the ideal height for this width and return it in the **cy** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67f1b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="67f1b-117">Return value</span></span>

<span data-ttu-id="67f1b-118">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="67f1b-118">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="67f1b-119">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="67f1b-119">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f1b-120">備註</span><span class="sxs-lookup"><span data-stu-id="67f1b-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="67f1b-121">如果您不想要任何特殊的按鈕寬度，則必須將 [**大小**](/previous-versions//dd145106(v=vs.85)) 的成員設定為零，以計算並傳回理想的高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="67f1b-121">If no special button width is desired, then you must set both members of [**SIZE**](/previous-versions//dd145106(v=vs.85)) to zero to calculate and return the ideal height and width.</span></span> <span data-ttu-id="67f1b-122">如果 **cx** 成員的值大於零，則會將這個值視為所需的按鈕寬度，並計算此寬度的理想高度，並在 **cy** 成員中傳回。</span><span class="sxs-lookup"><span data-stu-id="67f1b-122">If the value of the **cx** member is greater than zero, then this value is considered the desired button width, and the ideal height for this width is calculated and returned in the **cy** member.</span></span>

 

<span data-ttu-id="67f1b-123">這則訊息最適用于按鈕。</span><span class="sxs-lookup"><span data-stu-id="67f1b-123">This message is most applicable to PushButtons.</span></span> <span data-ttu-id="67f1b-124">傳送至按鈕時，訊息會抓取顯示按鈕文字所需的周框。</span><span class="sxs-lookup"><span data-stu-id="67f1b-124">When sent to a PushButton, the message retrieves the bounding rectangle required to display the button's text.</span></span> <span data-ttu-id="67f1b-125">此外，如果按鈕具有影像清單，周框也會調整大小以包含按鈕的影像。</span><span class="sxs-lookup"><span data-stu-id="67f1b-125">Additionally, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image.</span></span>

<span data-ttu-id="67f1b-126">傳送至任何其他類型的按鈕時，會抓取控制項的視窗矩形大小。</span><span class="sxs-lookup"><span data-stu-id="67f1b-126">When sent to a button of any other type, the size of the control's window rectangle is retrieved.</span></span>

> [!Note]  
> <span data-ttu-id="67f1b-127">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="67f1b-127">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="67f1b-128">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="67f1b-128">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67f1b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="67f1b-129">Requirements</span></span>



| <span data-ttu-id="67f1b-130">需求</span><span class="sxs-lookup"><span data-stu-id="67f1b-130">Requirement</span></span> | <span data-ttu-id="67f1b-131">值</span><span class="sxs-lookup"><span data-stu-id="67f1b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67f1b-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67f1b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="67f1b-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67f1b-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67f1b-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67f1b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="67f1b-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67f1b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67f1b-136">標頭</span><span class="sxs-lookup"><span data-stu-id="67f1b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="67f1b-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="67f1b-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

