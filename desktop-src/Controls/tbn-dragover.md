---
title: 'TBN_DRAGOVER (Commctrl 的通知碼) '
description: Ascertains 是否 \_ 應針對要拖曳的按鈕傳送一則 TB MARKBUTTON 訊息。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464765"
---
# <a name="tbn_dragover-notification-code"></a><span data-ttu-id="3aa2a-105">TBN \_ system.windows.dragdrop.dragover> 通知碼</span><span class="sxs-lookup"><span data-stu-id="3aa2a-105">TBN\_DRAGOVER notification code</span></span>

<span data-ttu-id="3aa2a-106">Ascertains 是否應針對要拖曳的按鈕傳送一則 [**TB \_ MARKBUTTON**](tb-markbutton.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="3aa2a-106">Ascertains whether a [**TB\_MARKBUTTON**](tb-markbutton.md) message should be sent for a button that is being dragged over.</span></span> <span data-ttu-id="3aa2a-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="3aa2a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3aa2a-108">參數</span><span class="sxs-lookup"><span data-stu-id="3aa2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa2a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3aa2a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa2a-110">[**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)結構的指標，指定要將哪些專案拖曳至其中。</span><span class="sxs-lookup"><span data-stu-id="3aa2a-110">A pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that specifies which item is being dragged over.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa2a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3aa2a-111">Return value</span></span>

<span data-ttu-id="3aa2a-112">如果工具列應該傳送 TB 的 MARKBUTTON 訊息，則為 **FALSE** ， \_ 否則為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="3aa2a-112">**FALSE** if the toolbar should send a TB\_MARKBUTTON message; otherwise **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa2a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3aa2a-113">Requirements</span></span>



| <span data-ttu-id="3aa2a-114">需求</span><span class="sxs-lookup"><span data-stu-id="3aa2a-114">Requirement</span></span> | <span data-ttu-id="3aa2a-115">值</span><span class="sxs-lookup"><span data-stu-id="3aa2a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa2a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3aa2a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa2a-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3aa2a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3aa2a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3aa2a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa2a-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3aa2a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3aa2a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3aa2a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aa2a-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa2a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





