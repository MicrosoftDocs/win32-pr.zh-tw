---
title: 'HDN_FILTERBTNCLICK (Commctrl 的通知碼) '
description: 當按一下 [篩選] 按鈕或回應 HDM SETITEM 訊息時，通知標題控制項的父視窗 \_ 。 此通知碼以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843151"
---
# <a name="hdn_filterbtnclick-notification-code"></a><span data-ttu-id="00d5d-105">HDN \_ FILTERBTNCLICK 通知碼</span><span class="sxs-lookup"><span data-stu-id="00d5d-105">HDN\_FILTERBTNCLICK notification code</span></span>

<span data-ttu-id="00d5d-106">當按一下 [篩選] 按鈕或回應 [**HDM \_ SETITEM**](hdm-setitem.md) 訊息時，通知標題控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="00d5d-106">Notifies the header control's parent window when the filter button is clicked or in response to an [**HDM\_SETITEM**](hdm-setitem.md) message.</span></span> <span data-ttu-id="00d5d-107">此通知碼以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="00d5d-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="00d5d-108">參數</span><span class="sxs-lookup"><span data-stu-id="00d5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d5d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00d5d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00d5d-110">[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)結構的指標，其中包含標題控制項和標頭篩選按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="00d5d-110">A pointer to an [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) structure that contains information about the header control and the header filter button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d5d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="00d5d-111">Return value</span></span>

<span data-ttu-id="00d5d-112">如果您傳回 **TRUE**， [HDN \_ FILTERCHANGE](hdn-filterchange.md) 通知碼將會傳送至標題控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="00d5d-112">If you return **TRUE**, an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification code will be sent to the header control's parent window.</span></span> <span data-ttu-id="00d5d-113">此通知碼可讓父視窗有機會同步處理其使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="00d5d-113">This notification code gives the parent window an opportunity to synchronize its user interface elements.</span></span> <span data-ttu-id="00d5d-114">如果您不想傳送通知，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="00d5d-114">Return **FALSE** if you do not want the notification sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="00d5d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="00d5d-115">Requirements</span></span>



| <span data-ttu-id="00d5d-116">需求</span><span class="sxs-lookup"><span data-stu-id="00d5d-116">Requirement</span></span> | <span data-ttu-id="00d5d-117">值</span><span class="sxs-lookup"><span data-stu-id="00d5d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00d5d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00d5d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00d5d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00d5d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00d5d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00d5d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00d5d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00d5d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00d5d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="00d5d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d5d-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="00d5d-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d5d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00d5d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d5d-125">**NMHDFILTERBTNCLICK**</span><span class="sxs-lookup"><span data-stu-id="00d5d-125">**NMHDFILTERBTNCLICK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





