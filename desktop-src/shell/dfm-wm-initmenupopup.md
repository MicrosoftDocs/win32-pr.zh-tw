---
description: 當下拉功能表或子功能表即將變成作用中時傳送。 這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。
title: 'DFM_WM_INITMENUPOPUP 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112336"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="a7292-104">DFM \_ WM \_ INITMENUPOPUP 訊息</span><span class="sxs-lookup"><span data-stu-id="a7292-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="a7292-105">當下拉功能表或子功能表即將變成作用中時傳送。</span><span class="sxs-lookup"><span data-stu-id="a7292-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="a7292-106">這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。</span><span class="sxs-lookup"><span data-stu-id="a7292-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="a7292-107">參數</span><span class="sxs-lookup"><span data-stu-id="a7292-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7292-108">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7292-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7292-109">下拉式功能表或子功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7292-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="a7292-110">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7292-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7292-111">低序位字組會指定開啟下拉式功能表或子功能表之功能表項目的以零為起始的相對位置。</span><span class="sxs-lookup"><span data-stu-id="a7292-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="a7292-112">高序位單字指出下拉式功能表是否為 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="a7292-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="a7292-113">如果功能表是 [視窗] 功能表，此參數為 **TRUE**;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a7292-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7292-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7292-114">Return value</span></span>

<span data-ttu-id="a7292-115">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a7292-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7292-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7292-116">Requirements</span></span>



| <span data-ttu-id="a7292-117">需求</span><span class="sxs-lookup"><span data-stu-id="a7292-117">Requirement</span></span> | <span data-ttu-id="a7292-118">值</span><span class="sxs-lookup"><span data-stu-id="a7292-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a7292-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7292-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a7292-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7292-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a7292-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7292-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a7292-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7292-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a7292-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a7292-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7292-124"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7292-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




