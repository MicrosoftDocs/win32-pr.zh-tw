---
title: 'TBN_DUPACCELERATOR (Commctrl 的通知碼) '
description: Ascertains 快速鍵是否可用於兩個或多個作用中的工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025325"
---
# <a name="tbn_dupaccelerator-notification-code"></a><span data-ttu-id="acb89-105">TBN \_ DUPACCELERATOR 通知碼</span><span class="sxs-lookup"><span data-stu-id="acb89-105">TBN\_DUPACCELERATOR notification code</span></span>

<span data-ttu-id="acb89-106">Ascertains 快速鍵是否可用於兩個或多個作用中的工具列。</span><span class="sxs-lookup"><span data-stu-id="acb89-106">Ascertains whether an accelerator key can be used on two or more active toolbars.</span></span> <span data-ttu-id="acb89-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="acb89-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="acb89-108">參數</span><span class="sxs-lookup"><span data-stu-id="acb89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acb89-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acb89-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acb89-110">結構的指標，此結構會提供快速鍵，並接收指定多個工具列是否回應相同字元的值。</span><span class="sxs-lookup"><span data-stu-id="acb89-110">A pointer to a structure that provides an accelerator and that receives a value specifying whether multiple toolbars respond to the same character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acb89-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="acb89-111">Return value</span></span>

<span data-ttu-id="acb89-112">如果成功則傳回 **TRUE** ，否則傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="acb89-112">Returns **TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="acb89-113">備註</span><span class="sxs-lookup"><span data-stu-id="acb89-113">Remarks</span></span>

<span data-ttu-id="acb89-114">應用程式必須宣告 **NMTBDUPACCELERATOR** 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="acb89-114">The application must declare the **NMTBDUPACCELERATOR** structure as follows:</span></span>

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="acb89-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="acb89-115">Requirements</span></span>



| <span data-ttu-id="acb89-116">需求</span><span class="sxs-lookup"><span data-stu-id="acb89-116">Requirement</span></span> | <span data-ttu-id="acb89-117">值</span><span class="sxs-lookup"><span data-stu-id="acb89-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acb89-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acb89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="acb89-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acb89-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="acb89-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acb89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="acb89-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acb89-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acb89-122">標頭</span><span class="sxs-lookup"><span data-stu-id="acb89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb89-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="acb89-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





