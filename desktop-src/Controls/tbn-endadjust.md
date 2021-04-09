---
title: 'TBN_ENDADJUST (Commctrl 的通知碼) '
description: 通知工具列的父視窗，指出使用者已停止自訂工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- TBN_ENDADJUST 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024986"
---
# <a name="tbn_endadjust-notification-code"></a><span data-ttu-id="c554e-105">TBN \_ ENDADJUST 通知碼</span><span class="sxs-lookup"><span data-stu-id="c554e-105">TBN\_ENDADJUST notification code</span></span>

<span data-ttu-id="c554e-106">通知工具列的父視窗，指出使用者已停止自訂工具列。</span><span class="sxs-lookup"><span data-stu-id="c554e-106">Notifies a toolbar's parent window that the user has stopped customizing a toolbar.</span></span> <span data-ttu-id="c554e-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="c554e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c554e-108">參數</span><span class="sxs-lookup"><span data-stu-id="c554e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c554e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c554e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c554e-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c554e-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c554e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c554e-111">Return value</span></span>

<span data-ttu-id="c554e-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="c554e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c554e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c554e-113">Requirements</span></span>



| <span data-ttu-id="c554e-114">需求</span><span class="sxs-lookup"><span data-stu-id="c554e-114">Requirement</span></span> | <span data-ttu-id="c554e-115">值</span><span class="sxs-lookup"><span data-stu-id="c554e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c554e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c554e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c554e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c554e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c554e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c554e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c554e-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c554e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c554e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c554e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c554e-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c554e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





