---
title: 'TBN_CUSTHELP (Commctrl 的通知碼) '
description: 通知工具列的父視窗，指出使用者已在 [自訂工具列] 對話方塊中選擇 [說明] 按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- TBN_CUSTHELP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843292"
---
# <a name="tbn_custhelp-notification-code"></a><span data-ttu-id="70bd0-105">TBN \_ CUSTHELP 通知碼</span><span class="sxs-lookup"><span data-stu-id="70bd0-105">TBN\_CUSTHELP notification code</span></span>

<span data-ttu-id="70bd0-106">通知工具列的父視窗，指出使用者已在 [自訂工具列] 對話方塊中選擇 [說明] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="70bd0-106">Notifies a toolbar's parent window that the user has chosen the Help button in the Customize Toolbar dialog box.</span></span> <span data-ttu-id="70bd0-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="70bd0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="70bd0-108">參數</span><span class="sxs-lookup"><span data-stu-id="70bd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70bd0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70bd0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70bd0-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70bd0-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70bd0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="70bd0-111">Return value</span></span>

<span data-ttu-id="70bd0-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="70bd0-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="70bd0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="70bd0-113">Requirements</span></span>



| <span data-ttu-id="70bd0-114">需求</span><span class="sxs-lookup"><span data-stu-id="70bd0-114">Requirement</span></span> | <span data-ttu-id="70bd0-115">值</span><span class="sxs-lookup"><span data-stu-id="70bd0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70bd0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70bd0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="70bd0-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70bd0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70bd0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70bd0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="70bd0-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70bd0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70bd0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="70bd0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="70bd0-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="70bd0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





