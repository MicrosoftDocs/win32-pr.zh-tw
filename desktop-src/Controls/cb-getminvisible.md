---
title: 'CB_GETMINVISIBLE 訊息 (Commctrl .h) '
description: 取得下拉式方塊下拉式清單中可見專案的最小數目。
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- CB_GETMINVISIBLE message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843567"
---
# <a name="cb_getminvisible-message"></a><span data-ttu-id="7228a-104">CB \_ GETMINVISIBLE 訊息</span><span class="sxs-lookup"><span data-stu-id="7228a-104">CB\_GETMINVISIBLE message</span></span>

<span data-ttu-id="7228a-105">取得下拉式方塊下拉式清單中可見專案的最小數目。</span><span class="sxs-lookup"><span data-stu-id="7228a-105">Gets the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="7228a-106">參數</span><span class="sxs-lookup"><span data-stu-id="7228a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7228a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7228a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7228a-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="7228a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7228a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7228a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7228a-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="7228a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7228a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7228a-111">Return value</span></span>

<span data-ttu-id="7228a-112">傳回值是可見專案的最小數目。</span><span class="sxs-lookup"><span data-stu-id="7228a-112">The return value is the minimum number of visible items.</span></span>

## <a name="remarks"></a><span data-ttu-id="7228a-113">備註</span><span class="sxs-lookup"><span data-stu-id="7228a-113">Remarks</span></span>

<span data-ttu-id="7228a-114">當下拉式清單中的專案數目大於最小值時，下拉式方塊就會使用捲軸。</span><span class="sxs-lookup"><span data-stu-id="7228a-114">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span>

<span data-ttu-id="7228a-115">如果下拉式方塊控制項的樣式為 [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md)，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="7228a-115">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="7228a-116">若要使用 **CB \_ GETMINVISIBLE**，應用程式必須在資訊清單中指定 comctl32.dll 第6版。</span><span class="sxs-lookup"><span data-stu-id="7228a-116">To use **CB\_GETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="7228a-117">如需詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="7228a-117">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7228a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7228a-118">Requirements</span></span>



| <span data-ttu-id="7228a-119">需求</span><span class="sxs-lookup"><span data-stu-id="7228a-119">Requirement</span></span> | <span data-ttu-id="7228a-120">值</span><span class="sxs-lookup"><span data-stu-id="7228a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7228a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7228a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7228a-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7228a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7228a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7228a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7228a-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7228a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7228a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7228a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7228a-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7228a-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7228a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7228a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7228a-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="7228a-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7228a-129">**CB \_ SETMINVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="7228a-129">**CB\_SETMINVISIBLE**</span></span>](cb-setminvisible.md)
</dt> <dt>

[<span data-ttu-id="7228a-130">**ComboBox \_ GetMinVisible**</span><span class="sxs-lookup"><span data-stu-id="7228a-130">**ComboBox\_GetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





