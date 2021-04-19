---
title: 'TBN_INITCUSTOMIZE (Commctrl 的通知碼) '
description: 通知工具列的父視窗，自訂已開始。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966283"
---
# <a name="tbn_initcustomize-notification-code"></a><span data-ttu-id="00c3d-105">TBN \_ INITCUSTOMIZE 通知碼</span><span class="sxs-lookup"><span data-stu-id="00c3d-105">TBN\_INITCUSTOMIZE notification code</span></span>

<span data-ttu-id="00c3d-106">通知工具列的父視窗，自訂已開始。</span><span class="sxs-lookup"><span data-stu-id="00c3d-106">Notifies a toolbar's parent window that customizing has started.</span></span> <span data-ttu-id="00c3d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="00c3d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="00c3d-108">參數</span><span class="sxs-lookup"><span data-stu-id="00c3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c3d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00c3d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00c3d-110">工具列 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="00c3d-110">Pointer to the toolbar's [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c3d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="00c3d-111">Return value</span></span>

<span data-ttu-id="00c3d-112">傳回 TBNRF \_ HIDEHELP 來隱藏 [說明] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="00c3d-112">Returns TBNRF\_HIDEHELP to suppress the Help button.</span></span>

## <a name="requirements"></a><span data-ttu-id="00c3d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="00c3d-113">Requirements</span></span>



| <span data-ttu-id="00c3d-114">需求</span><span class="sxs-lookup"><span data-stu-id="00c3d-114">Requirement</span></span> | <span data-ttu-id="00c3d-115">值</span><span class="sxs-lookup"><span data-stu-id="00c3d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00c3d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00c3d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="00c3d-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00c3d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00c3d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00c3d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="00c3d-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00c3d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00c3d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="00c3d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="00c3d-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="00c3d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





