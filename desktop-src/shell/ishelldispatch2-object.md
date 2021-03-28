---
description: 使用各種新功能來擴充 IShellDispatch 物件。
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: 'IShellDispatch2 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972388"
---
# <a name="ishelldispatch2-object"></a><span data-ttu-id="7115d-103">IShellDispatch2 物件</span><span class="sxs-lookup"><span data-stu-id="7115d-103">IShellDispatch2 object</span></span>

<span data-ttu-id="7115d-104">使用各種新功能來擴充 [**IShellDispatch**](ishelldispatch.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7115d-104">Extends the [**IShellDispatch**](ishelldispatch.md) object with a variety of new functionality.</span></span>

> [!Note]  
> <span data-ttu-id="7115d-105">**IShellDispatch2** 是透過 [**Shell**](shell.md) 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="7115d-105">**IShellDispatch2** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="7115d-106">成員</span><span class="sxs-lookup"><span data-stu-id="7115d-106">Members</span></span>

<span data-ttu-id="7115d-107">**IShellDispatch2** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7115d-107">The **IShellDispatch2** object has these types of members:</span></span>

-   [<span data-ttu-id="7115d-108">方法</span><span class="sxs-lookup"><span data-stu-id="7115d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7115d-109">方法</span><span class="sxs-lookup"><span data-stu-id="7115d-109">Methods</span></span>

<span data-ttu-id="7115d-110">**IShellDispatch2** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7115d-110">The **IShellDispatch2** object has these methods.</span></span>



| <span data-ttu-id="7115d-111">方法</span><span class="sxs-lookup"><span data-stu-id="7115d-111">Method</span></span>                                                               | <span data-ttu-id="7115d-112">描述</span><span class="sxs-lookup"><span data-stu-id="7115d-112">Description</span></span>                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="7115d-113">**CanStartStopService**</span><span class="sxs-lookup"><span data-stu-id="7115d-113">**CanStartStopService**</span></span>](ishelldispatch2-canstartstopservice.md)   | <span data-ttu-id="7115d-114">判斷目前的使用者是否可以啟動和停止命名服務。</span><span class="sxs-lookup"><span data-stu-id="7115d-114">Determines if the current user can start and stop the named service.</span></span><br/>    |
| [<span data-ttu-id="7115d-115">**FindPrinter**</span><span class="sxs-lookup"><span data-stu-id="7115d-115">**FindPrinter**</span></span>](ishelldispatch2-findprinter.md)                   | <span data-ttu-id="7115d-116">顯示 [ **尋找印表機** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7115d-116">Displays the **Find Printer** dialog box.</span></span><br/>                               |
| [<span data-ttu-id="7115d-117">**GetSystemInformation**</span><span class="sxs-lookup"><span data-stu-id="7115d-117">**GetSystemInformation**</span></span>](ishelldispatch2-getsysteminformation.md) | <span data-ttu-id="7115d-118">捕獲系統資訊。</span><span class="sxs-lookup"><span data-stu-id="7115d-118">Retrieves system information.</span></span><br/>                                           |
| [<span data-ttu-id="7115d-119">**IsRestricted**</span><span class="sxs-lookup"><span data-stu-id="7115d-119">**IsRestricted**</span></span>](ishelldispatch2-isrestricted.md)                 | <span data-ttu-id="7115d-120">從登錄抓取群組的限制設定。</span><span class="sxs-lookup"><span data-stu-id="7115d-120">Retrieves a group's restriction setting from the registry.</span></span><br/>              |
| [<span data-ttu-id="7115d-121">**IsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="7115d-121">**IsServiceRunning**</span></span>](ishelldispatch2-isservicerunning.md)         | <span data-ttu-id="7115d-122">傳回值，這個值表示特定服務是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="7115d-122">Returns a value that indicates whether a particular service is running.</span></span><br/> |
| [<span data-ttu-id="7115d-123">**ServiceStart**</span><span class="sxs-lookup"><span data-stu-id="7115d-123">**ServiceStart**</span></span>](ishelldispatch2-servicestart.md)                 | <span data-ttu-id="7115d-124">啟動命名服務。</span><span class="sxs-lookup"><span data-stu-id="7115d-124">Starts a named service.</span></span><br/>                                                 |
| [<span data-ttu-id="7115d-125">**ServiceStop**</span><span class="sxs-lookup"><span data-stu-id="7115d-125">**ServiceStop**</span></span>](ishelldispatch2-servicestop.md)                   | <span data-ttu-id="7115d-126">停止已命名的服務。</span><span class="sxs-lookup"><span data-stu-id="7115d-126">Stops a named service.</span></span><br/>                                                  |
| [<span data-ttu-id="7115d-127">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="7115d-127">**ShellExecute**</span></span>](ishelldispatch2-shellexecute.md)                 | <span data-ttu-id="7115d-128">在指定的檔案上執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="7115d-128">Performs a specified operation on a specified file.</span></span><br/>                     |
| [<span data-ttu-id="7115d-129">**ShowBrowserBar**</span><span class="sxs-lookup"><span data-stu-id="7115d-129">**ShowBrowserBar**</span></span>](ishelldispatch2-showbrowserbar.md)             | <span data-ttu-id="7115d-130">顯示瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="7115d-130">Displays a browser bar.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="7115d-131">備註</span><span class="sxs-lookup"><span data-stu-id="7115d-131">Remarks</span></span>

<span data-ttu-id="7115d-132">如需 Windows 服務的討論，請參閱 [服務](../services/services.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="7115d-132">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="7115d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7115d-133">Requirements</span></span>



| <span data-ttu-id="7115d-134">需求</span><span class="sxs-lookup"><span data-stu-id="7115d-134">Requirement</span></span> | <span data-ttu-id="7115d-135">值</span><span class="sxs-lookup"><span data-stu-id="7115d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7115d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7115d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7115d-137">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7115d-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7115d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7115d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7115d-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7115d-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7115d-140">標頭</span><span class="sxs-lookup"><span data-stu-id="7115d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7115d-141"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7115d-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7115d-142">Idl</span><span class="sxs-lookup"><span data-stu-id="7115d-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7115d-143"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7115d-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7115d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7115d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7115d-145"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7115d-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7115d-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7115d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7115d-147">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="7115d-147">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="7115d-148">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="7115d-148">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="7115d-149">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="7115d-149">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> </dl>

 

 
