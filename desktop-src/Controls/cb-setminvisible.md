---
title: 'CB_SETMINVISIBLE 訊息 (Commctrl .h) '
description: 應用程式會傳送 CB \_ SETMINVISIBLE 訊息，在下拉式方塊的下拉式清單中設定可見專案的最小數目。
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093935"
---
# <a name="cb_setminvisible-message"></a><span data-ttu-id="59bb2-104">CB \_ SETMINVISIBLE 訊息</span><span class="sxs-lookup"><span data-stu-id="59bb2-104">CB\_SETMINVISIBLE message</span></span>

<span data-ttu-id="59bb2-105">應用程式會傳送 **CB \_ SETMINVISIBLE** 訊息，在下拉式方塊的下拉式清單中設定可見專案的最小數目。</span><span class="sxs-lookup"><span data-stu-id="59bb2-105">An application sends a **CB\_SETMINVISIBLE** message to set the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="59bb2-106">參數</span><span class="sxs-lookup"><span data-stu-id="59bb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59bb2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59bb2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59bb2-108">指定可見專案的最小數目。</span><span class="sxs-lookup"><span data-stu-id="59bb2-108">Specifies the minimum number of visible items.</span></span>

</dd> <dt>

<span data-ttu-id="59bb2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59bb2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59bb2-110">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="59bb2-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59bb2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="59bb2-111">Return value</span></span>

<span data-ttu-id="59bb2-112">如果訊息成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="59bb2-112">If the message is successful, the return value is **TRUE**.</span></span> <span data-ttu-id="59bb2-113">否則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="59bb2-113">Otherwise the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="59bb2-114">備註</span><span class="sxs-lookup"><span data-stu-id="59bb2-114">Remarks</span></span>

<span data-ttu-id="59bb2-115">當下拉式清單中的專案數目大於最小值時，下拉式方塊就會使用捲軸。</span><span class="sxs-lookup"><span data-stu-id="59bb2-115">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span> <span data-ttu-id="59bb2-116">根據預設，30是可見專案的最小數目。</span><span class="sxs-lookup"><span data-stu-id="59bb2-116">By default, 30 is the minimum number of visible items.</span></span>

<span data-ttu-id="59bb2-117">如果下拉式方塊控制項的樣式為 [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md)，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="59bb2-117">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="59bb2-118">若要使用 **CB \_ SETMINVISIBLE**，應用程式必須在資訊清單中指定 comctl32.dll 第6版。</span><span class="sxs-lookup"><span data-stu-id="59bb2-118">To use **CB\_SETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="59bb2-119">如需詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="59bb2-119">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59bb2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="59bb2-120">Requirements</span></span>



| <span data-ttu-id="59bb2-121">需求</span><span class="sxs-lookup"><span data-stu-id="59bb2-121">Requirement</span></span> | <span data-ttu-id="59bb2-122">值</span><span class="sxs-lookup"><span data-stu-id="59bb2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59bb2-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59bb2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59bb2-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59bb2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59bb2-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59bb2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59bb2-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59bb2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59bb2-127">標頭</span><span class="sxs-lookup"><span data-stu-id="59bb2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="59bb2-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="59bb2-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59bb2-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59bb2-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="59bb2-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="59bb2-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="59bb2-131">**CB \_ GETMINVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="59bb2-131">**CB\_GETMINVISIBLE**</span></span>](cb-getminvisible.md)
</dt> <dt>

[<span data-ttu-id="59bb2-132">**ComboBox \_ SetMinVisible**</span><span class="sxs-lookup"><span data-stu-id="59bb2-132">**ComboBox\_SetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





