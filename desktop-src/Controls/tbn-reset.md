---
title: 'TBN_RESET (Commctrl 的通知碼) '
description: 通知工具列的父視窗，指出使用者已重設 [自訂工具列] 對話方塊的內容。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025437"
---
# <a name="tbn_reset-notification-code"></a><span data-ttu-id="2ff21-105">TBN \_ 重設通知碼</span><span class="sxs-lookup"><span data-stu-id="2ff21-105">TBN\_RESET notification code</span></span>

<span data-ttu-id="2ff21-106">通知工具列的父視窗，指出使用者已重設 [自訂工具列] 對話方塊的內容。</span><span class="sxs-lookup"><span data-stu-id="2ff21-106">Notifies the toolbar's parent window that the user has reset the content of the Customize Toolbar dialog box.</span></span> <span data-ttu-id="2ff21-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="2ff21-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2ff21-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ff21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff21-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ff21-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ff21-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2ff21-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff21-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ff21-111">Return value</span></span>

<span data-ttu-id="2ff21-112">返回 \_ [TBNRF ENDCUSTOMIZE] 以關閉 [自訂工具列] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2ff21-112">Return TBNRF\_ENDCUSTOMIZE to close the Customize Toolbar dialog box.</span></span> <span data-ttu-id="2ff21-113">所有其他傳回值都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2ff21-113">All other return values are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff21-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ff21-114">Requirements</span></span>



| <span data-ttu-id="2ff21-115">需求</span><span class="sxs-lookup"><span data-stu-id="2ff21-115">Requirement</span></span> | <span data-ttu-id="2ff21-116">值</span><span class="sxs-lookup"><span data-stu-id="2ff21-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff21-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ff21-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff21-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ff21-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ff21-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ff21-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff21-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ff21-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ff21-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2ff21-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ff21-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff21-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





