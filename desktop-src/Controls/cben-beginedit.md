---
title: 'CBEN_BEGINEDIT (Commctrl 的通知碼) '
description: 當使用者啟動下拉式清單，或按一下控制項的編輯方塊時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- CBEN_BEGINEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d4cc80d12b01b9374173f413f0aee3701e5040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970002"
---
# <a name="cben_beginedit-notification-code"></a><span data-ttu-id="cc63e-105">CBEN \_ BEGINEDIT 通知碼</span><span class="sxs-lookup"><span data-stu-id="cc63e-105">CBEN\_BEGINEDIT notification code</span></span>

<span data-ttu-id="cc63e-106">當使用者啟動下拉式清單，或按一下控制項的編輯方塊時傳送。</span><span class="sxs-lookup"><span data-stu-id="cc63e-106">Sent when the user activates the drop-down list or clicks in the control's edit box.</span></span> <span data-ttu-id="cc63e-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="cc63e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cc63e-108">參數</span><span class="sxs-lookup"><span data-stu-id="cc63e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc63e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc63e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc63e-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cc63e-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc63e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc63e-111">Return value</span></span>

<span data-ttu-id="cc63e-112">處理此通知程式碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="cc63e-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc63e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc63e-113">Requirements</span></span>



| <span data-ttu-id="cc63e-114">需求</span><span class="sxs-lookup"><span data-stu-id="cc63e-114">Requirement</span></span> | <span data-ttu-id="cc63e-115">值</span><span class="sxs-lookup"><span data-stu-id="cc63e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc63e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc63e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cc63e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc63e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc63e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc63e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cc63e-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc63e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc63e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cc63e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc63e-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc63e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





