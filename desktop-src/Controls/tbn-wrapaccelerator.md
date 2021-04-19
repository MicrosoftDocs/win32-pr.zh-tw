---
title: 'TBN_WRAPACCELERATOR (Commctrl 的通知碼) '
description: 要求一或多個工具列中，對應至指定之快速鍵的按鈕索引。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001101"
---
# <a name="tbn_wrapaccelerator-notification-code"></a><span data-ttu-id="0df19-105">TBN \_ WRAPACCELERATOR 通知碼</span><span class="sxs-lookup"><span data-stu-id="0df19-105">TBN\_WRAPACCELERATOR notification code</span></span>

<span data-ttu-id="0df19-106">要求一或多個工具列中，對應至指定之快速鍵的按鈕索引。</span><span class="sxs-lookup"><span data-stu-id="0df19-106">Requests the index of the button in one or more toolbars corresponding to the specified accelerator character.</span></span> <span data-ttu-id="0df19-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="0df19-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0df19-108">參數</span><span class="sxs-lookup"><span data-stu-id="0df19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df19-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0df19-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0df19-110">結構的指標，其中包含快速鍵字元，並會接收對應按鈕的索引。</span><span class="sxs-lookup"><span data-stu-id="0df19-110">A pointer to a structure that contains the accelerator key character, and that receives the index of the corresponding button.</span></span> <span data-ttu-id="0df19-111">如果快速鍵未對應至命令，則索引為-1。</span><span class="sxs-lookup"><span data-stu-id="0df19-111">The index is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df19-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0df19-112">Return value</span></span>

<span data-ttu-id="0df19-113">如果傳回索引，則 **為 TRUE** ，否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0df19-113">**TRUE** if an index is returned, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0df19-114">備註</span><span class="sxs-lookup"><span data-stu-id="0df19-114">Remarks</span></span>

<span data-ttu-id="0df19-115">具有一或多個工具列的應用程式可能會收到此通知碼。</span><span class="sxs-lookup"><span data-stu-id="0df19-115">Applications with one or more toolbars may receive this notification code.</span></span>

<span data-ttu-id="0df19-116">**NMTBWRAPACCELERATOR** 結構必須由應用程式定義，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0df19-116">The **NMTBWRAPACCELERATOR** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="0df19-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0df19-117">Requirements</span></span>



| <span data-ttu-id="0df19-118">需求</span><span class="sxs-lookup"><span data-stu-id="0df19-118">Requirement</span></span> | <span data-ttu-id="0df19-119">值</span><span class="sxs-lookup"><span data-stu-id="0df19-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0df19-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0df19-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0df19-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0df19-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0df19-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0df19-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0df19-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0df19-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0df19-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0df19-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df19-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0df19-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





