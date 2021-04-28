---
description: DFM_WM_INITMENUPOPUP 訊息-在下拉式功能表或子功能表即將變成作用中時傳送。 這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。
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
ms.openlocfilehash: 9df2700403dcdc0ce00b6d90d9c3a87d373b0a34
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096996"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="74428-104">DFM \_ WM \_ INITMENUPOPUP 訊息</span><span class="sxs-lookup"><span data-stu-id="74428-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="74428-105">當下拉功能表或子功能表即將變成作用中時傳送。</span><span class="sxs-lookup"><span data-stu-id="74428-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="74428-106">這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。</span><span class="sxs-lookup"><span data-stu-id="74428-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="74428-107">參數</span><span class="sxs-lookup"><span data-stu-id="74428-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74428-108">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74428-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74428-109">下拉式功能表或子功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="74428-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="74428-110">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74428-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74428-111">低序位字組會指定開啟下拉式功能表或子功能表之功能表項目的以零為起始的相對位置。</span><span class="sxs-lookup"><span data-stu-id="74428-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="74428-112">高序位單字指出下拉式功能表是否為 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="74428-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="74428-113">如果功能表是 [視窗] 功能表，此參數為 **TRUE**;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="74428-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74428-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="74428-114">Return value</span></span>

<span data-ttu-id="74428-115">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="74428-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="74428-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="74428-116">Requirements</span></span>



| <span data-ttu-id="74428-117">需求</span><span class="sxs-lookup"><span data-stu-id="74428-117">Requirement</span></span> | <span data-ttu-id="74428-118">值</span><span class="sxs-lookup"><span data-stu-id="74428-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74428-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74428-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74428-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74428-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="74428-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74428-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74428-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74428-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74428-123">標頭</span><span class="sxs-lookup"><span data-stu-id="74428-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="74428-124"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="74428-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




