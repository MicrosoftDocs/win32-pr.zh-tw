---
title: 'NM_CUSTOMDRAW (按鈕) 通知碼 (Commctrl) '
description: 通知按鈕控制項的父視窗，有關按鈕上的自訂繪製作業。 按鈕控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- NM_CUSTOMDRAW (按鈕) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467113"
---
# <a name="nm_customdraw-button-notification-code"></a><span data-ttu-id="efa34-105">NM \_ CUSTOMDRAW (按鈕) 通知碼</span><span class="sxs-lookup"><span data-stu-id="efa34-105">NM\_CUSTOMDRAW (button) notification code</span></span>

<span data-ttu-id="efa34-106">通知按鈕控制項的父視窗，有關按鈕上的自訂繪製作業。</span><span class="sxs-lookup"><span data-stu-id="efa34-106">Notifies the parent window of a button control about custom draw operations on the button.</span></span>

<span data-ttu-id="efa34-107">按鈕控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="efa34-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="efa34-108">參數</span><span class="sxs-lookup"><span data-stu-id="efa34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efa34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efa34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efa34-110">[**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="efa34-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="efa34-111">此結構的 **dwItemSpec** 成員包含所繪製專案的索引，而且此結構的 **lItemlParam** 成員包含該專案的 *lParam*。</span><span class="sxs-lookup"><span data-stu-id="efa34-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efa34-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="efa34-112">Return value</span></span>

<span data-ttu-id="efa34-113">您的應用程式可以傳回的值取決於目前的繪圖階段。</span><span class="sxs-lookup"><span data-stu-id="efa34-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="efa34-114">相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。</span><span class="sxs-lookup"><span data-stu-id="efa34-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="efa34-115">您必須傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="efa34-115">You must return one of the following values.</span></span>



| <span data-ttu-id="efa34-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="efa34-116">Return code</span></span>                                                                                          | <span data-ttu-id="efa34-117">Description</span><span class="sxs-lookup"><span data-stu-id="efa34-117">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="efa34-118"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="efa34-118"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl> | <span data-ttu-id="efa34-119">控制項將會在清除專案之後通知父代。</span><span class="sxs-lookup"><span data-stu-id="efa34-119">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="efa34-120">只有在 **dwDrawStage** 等於 CDDS PREERASE 時，才可以使用此 \_ 。</span><span class="sxs-lookup"><span data-stu-id="efa34-120">This can be used only if **dwDrawStage** equals CDDS\_PREERASE.</span></span><br/>                                  |
| <dl> <span data-ttu-id="efa34-121"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="efa34-121"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl> | <span data-ttu-id="efa34-122">控制項將會在繪製專案之後通知父系。</span><span class="sxs-lookup"><span data-stu-id="efa34-122">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="efa34-123">只有在 **dwDrawStage** 等於 CDDS PREPAINT 時，才可以使用此 \_ 。</span><span class="sxs-lookup"><span data-stu-id="efa34-123">This can be used only if **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                 |
| <dl> <span data-ttu-id="efa34-124"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="efa34-124"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>     | <span data-ttu-id="efa34-125">應用程式會以手動方式繪製專案。</span><span class="sxs-lookup"><span data-stu-id="efa34-125">The application drew the item manually.</span></span> <span data-ttu-id="efa34-126">控制項不會繪製專案。</span><span class="sxs-lookup"><span data-stu-id="efa34-126">The control will not draw the item.</span></span> <span data-ttu-id="efa34-127">這可在 **dwDrawStage** 等於 CDDS \_ PREERASE 或 CDDS PREPAINT 時使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="efa34-127">This can be used when **dwDrawStage** equals CDDS\_PREERASE or CDDS\_PREPAINT.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efa34-128">備註</span><span class="sxs-lookup"><span data-stu-id="efa34-128">Remarks</span></span>

<span data-ttu-id="efa34-129">如果按鈕控制項標示為 ownerdraw (BS \_ ownerdraw) ，則 \_ 不會傳送 NM CUSTOMDRAW 通知碼。</span><span class="sxs-lookup"><span data-stu-id="efa34-129">If the button control is marked ownerdraw (BS\_OWNERDRAW), the NM\_CUSTOMDRAW notification code is not sent.</span></span>

<span data-ttu-id="efa34-130">請參閱 [使用自訂繪製](custom-draw.md) 來進一步討論。</span><span class="sxs-lookup"><span data-stu-id="efa34-130">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

> [!Note]  
> <span data-ttu-id="efa34-131">若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="efa34-131">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="efa34-132">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="efa34-132">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="efa34-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="efa34-133">Requirements</span></span>



| <span data-ttu-id="efa34-134">需求</span><span class="sxs-lookup"><span data-stu-id="efa34-134">Requirement</span></span> | <span data-ttu-id="efa34-135">值</span><span class="sxs-lookup"><span data-stu-id="efa34-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa34-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="efa34-136">Minimum supported client</span></span><br/> | <span data-ttu-id="efa34-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efa34-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="efa34-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="efa34-138">Minimum supported server</span></span><br/> | <span data-ttu-id="efa34-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efa34-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="efa34-140">標頭</span><span class="sxs-lookup"><span data-stu-id="efa34-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="efa34-141"><dt>Commctrl (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="efa34-141"><dt>Commctrl.h (include Windows.h)</dt></span></span> </dl> |



 

 





