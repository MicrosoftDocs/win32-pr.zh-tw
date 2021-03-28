---
description: SFVM \_ GETPANE 可能已變更或無法使用。
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: 'SFVM_GETPANE 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944582"
---
# <a name="sfvm_getpane-message"></a><span data-ttu-id="a8f6c-103">SFVM \_ GETPANE 訊息</span><span class="sxs-lookup"><span data-stu-id="a8f6c-103">SFVM\_GETPANE message</span></span>

<span data-ttu-id="a8f6c-104">\[**SFVM \_GETPANE** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-104">\[**SFVM\_GETPANE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8f6c-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a8f6c-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="a8f6c-106">允許回呼物件提供狀態列窗格，以顯示網際網路區域資訊。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-106">Allows the callback object to provide the status bar pane in which to display the Internet zone information.</span></span> <span data-ttu-id="a8f6c-107">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a><span data-ttu-id="a8f6c-108">參數</span><span class="sxs-lookup"><span data-stu-id="a8f6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f6c-109">*paneID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8f6c-109">*paneID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f6c-110">要求之窗格的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-110">ID of the requested pane.</span></span> <span data-ttu-id="a8f6c-111">這通常是窗格 \_ 區域，但可以是下列任何一個值。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-111">This is normally PANE\_ZONE, but can be any one of the following values.</span></span>

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span data-ttu-id="a8f6c-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**窗格 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="a8f6c-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**PANE\_NONE**</span></span>


</dt> <dd>

<span data-ttu-id="a8f6c-113">沒有窗格。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-113">No pane.</span></span>

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span data-ttu-id="a8f6c-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**窗格 \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="a8f6c-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**PANE\_ZONE**</span></span>


</dt> <dd>

<span data-ttu-id="a8f6c-115">[網際網路區域] 窗格。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-115">The Internet zone pane.</span></span>

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span data-ttu-id="a8f6c-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**窗格 \_ 離線**</span><span class="sxs-lookup"><span data-stu-id="a8f6c-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANE\_OFFLINE**</span></span>


</dt> <dd>

<span data-ttu-id="a8f6c-117">離線窗格。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-117">The offline pane.</span></span>

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span data-ttu-id="a8f6c-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**窗格 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="a8f6c-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**PANE\_PRINTER**</span></span>


</dt> <dd>

<span data-ttu-id="a8f6c-119">列印指示窗格。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-119">The print indication pane.</span></span>

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span data-ttu-id="a8f6c-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**窗格 \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="a8f6c-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANE\_SSL**</span></span>


</dt> <dd>

<span data-ttu-id="a8f6c-121">SSL 窗格。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-121">The SSL pane.</span></span>

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span data-ttu-id="a8f6c-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**窗格 \_ 流覽**</span><span class="sxs-lookup"><span data-stu-id="a8f6c-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**PANE\_NAVIGATION**</span></span>


</dt> <dd>

<span data-ttu-id="a8f6c-123">流覽窗格。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-123">The navigation pane.</span></span>

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span data-ttu-id="a8f6c-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**窗格 \_ 進度**</span><span class="sxs-lookup"><span data-stu-id="a8f6c-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**PANE\_PROGRESS**</span></span>


</dt> <dd>

<span data-ttu-id="a8f6c-125">進度列窗格。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-125">The progress bar pane.</span></span>

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span data-ttu-id="a8f6c-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**窗格 \_ 隱私權**</span><span class="sxs-lookup"><span data-stu-id="a8f6c-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PANE\_PRIVACY**</span></span>


</dt> <dd>

<span data-ttu-id="a8f6c-127">隱私權指標窗格。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-127">The privacy indicator pane.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a8f6c-128">*窗格* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a8f6c-128">*pane* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f6c-129">包含窗格編號的 **DWORD** 指標。</span><span class="sxs-lookup"><span data-stu-id="a8f6c-129">Pointer to a **DWORD** containing the pane number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8f6c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8f6c-130">Requirements</span></span>



| <span data-ttu-id="a8f6c-131">需求</span><span class="sxs-lookup"><span data-stu-id="a8f6c-131">Requirement</span></span> | <span data-ttu-id="a8f6c-132">值</span><span class="sxs-lookup"><span data-stu-id="a8f6c-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f6c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8f6c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f6c-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8f6c-134">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a8f6c-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8f6c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f6c-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8f6c-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a8f6c-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a8f6c-137">End of client support</span></span><br/>    | <span data-ttu-id="a8f6c-138">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="a8f6c-138">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="a8f6c-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a8f6c-139">End of server support</span></span><br/>    | <span data-ttu-id="a8f6c-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8f6c-140">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="a8f6c-141">標頭</span><span class="sxs-lookup"><span data-stu-id="a8f6c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8f6c-142"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f6c-142"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
