---
title: 'TVN_SINGLEEXPAND (Commctrl 的通知碼) '
description: '\_當使用者使用滑鼠按一下來開啟或關閉樹狀專案時，由具有電視 SINGLEEXPAND 樣式的樹狀檢視控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。'
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464660"
---
# <a name="tvn_singleexpand-notification-code"></a><span data-ttu-id="a5386-105">IZDEBSKI \_ SINGLEEXPAND 通知碼</span><span class="sxs-lookup"><span data-stu-id="a5386-105">TVN\_SINGLEEXPAND notification code</span></span>

<span data-ttu-id="a5386-106">當使用者使用滑鼠按一下來開啟或關閉樹狀專案時，由具有 [**電視 \_ SINGLEEXPAND**](tree-view-control-window-styles.md) 樣式的樹狀檢視控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="a5386-106">Sent by a tree-view control with the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style when the user opens or closes a tree item using a single click of the mouse.</span></span> <span data-ttu-id="a5386-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a5386-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a><span data-ttu-id="a5386-108">參數</span><span class="sxs-lookup"><span data-stu-id="a5386-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5386-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5386-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5386-110">[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5386-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5386-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5386-111">Return value</span></span>

<span data-ttu-id="a5386-112">傳回 TVNRET \_ 預設值，以允許發生預設行為。</span><span class="sxs-lookup"><span data-stu-id="a5386-112">Return TVNRET\_DEFAULT to allow the default behavior to occur.</span></span> <span data-ttu-id="a5386-113">若要修改預設行為，請傳回：</span><span class="sxs-lookup"><span data-stu-id="a5386-113">To modify the default behavior, return:</span></span>



| <span data-ttu-id="a5386-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a5386-114">Return code</span></span>                                                                                    | <span data-ttu-id="a5386-115">Description</span><span class="sxs-lookup"><span data-stu-id="a5386-115">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5386-116"><dt>**TVNRET \_ SKIPOLD**</dt></span><span class="sxs-lookup"><span data-stu-id="a5386-116"><dt>**TVNRET\_SKIPOLD**</dt></span></span> </dl> | <span data-ttu-id="a5386-117">略過未選取專案的預設處理。</span><span class="sxs-lookup"><span data-stu-id="a5386-117">Skip default processing of the item being unselected.</span></span><br/> |
| <dl> <span data-ttu-id="a5386-118"><dt>**TVNRET \_ SKIPNEW**</dt></span><span class="sxs-lookup"><span data-stu-id="a5386-118"><dt>**TVNRET\_SKIPNEW**</dt></span></span> </dl> | <span data-ttu-id="a5386-119">略過選取專案的預設處理。</span><span class="sxs-lookup"><span data-stu-id="a5386-119">Skip default processing of the item being selected.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="a5386-120">備註</span><span class="sxs-lookup"><span data-stu-id="a5386-120">Remarks</span></span>

<span data-ttu-id="a5386-121">若要略過選取和未選取專案的預設處理，請將 TVNRET \_ SKIPOLD 和 TVNRET \_ SKIPNEW 與邏輯 OR 結合來傳回。</span><span class="sxs-lookup"><span data-stu-id="a5386-121">To skip default processing of selected and unselected items, return both TVNRET\_SKIPOLD and TVNRET\_SKIPNEW by combining them with a logical OR.</span></span>

<span data-ttu-id="a5386-122">只有具有 [**電視 \_ SINGLEEXPAND**](tree-view-control-window-styles.md) 樣式的樹狀檢視控制項才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="a5386-122">This notification code is only sent by tree-view controls that have the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5386-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5386-123">Requirements</span></span>



| <span data-ttu-id="a5386-124">需求</span><span class="sxs-lookup"><span data-stu-id="a5386-124">Requirement</span></span> | <span data-ttu-id="a5386-125">值</span><span class="sxs-lookup"><span data-stu-id="a5386-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5386-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5386-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5386-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5386-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5386-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5386-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5386-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5386-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5386-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a5386-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5386-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5386-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





