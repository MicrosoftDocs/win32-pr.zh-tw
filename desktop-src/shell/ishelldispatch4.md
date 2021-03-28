---
description: 擴充 IShellDispatch3 物件。
title: 'IShellDispatch4 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: 0bdada12a48f9c48749b614e6b45ff5427e62b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512209"
---
# <a name="ishelldispatch4-object"></a><span data-ttu-id="a7526-103">IShellDispatch4 物件</span><span class="sxs-lookup"><span data-stu-id="a7526-103">IShellDispatch4 object</span></span>

<span data-ttu-id="a7526-104">擴充 [**IShellDispatch3**](ishelldispatch3.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a7526-104">Extends the [**IShellDispatch3**](ishelldispatch3.md) object.</span></span> <span data-ttu-id="a7526-105">除了 **IShellDispatch3** 支援的屬性和方法之外， **IShellDispatch4** 還支援四個額外的方法。</span><span class="sxs-lookup"><span data-stu-id="a7526-105">In addition to the properties and methods supported by **IShellDispatch3**, **IShellDispatch4** supports four additional methods.</span></span>

> [!Note]  
> <span data-ttu-id="a7526-106">**IShellDispatch4** 是透過 [**Shell**](shell.md) 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="a7526-106">**IShellDispatch4** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="a7526-107">成員</span><span class="sxs-lookup"><span data-stu-id="a7526-107">Members</span></span>

<span data-ttu-id="a7526-108">**IShellDispatch4** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a7526-108">The **IShellDispatch4** object has these types of members:</span></span>

-   [<span data-ttu-id="a7526-109">方法</span><span class="sxs-lookup"><span data-stu-id="a7526-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a7526-110">方法</span><span class="sxs-lookup"><span data-stu-id="a7526-110">Methods</span></span>

<span data-ttu-id="a7526-111">**IShellDispatch4** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a7526-111">The **IShellDispatch4** object has these methods.</span></span>



| <span data-ttu-id="a7526-112">方法</span><span class="sxs-lookup"><span data-stu-id="a7526-112">Method</span></span>                                                     | <span data-ttu-id="a7526-113">描述</span><span class="sxs-lookup"><span data-stu-id="a7526-113">Description</span></span>                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="a7526-114">**ExplorerPolicy**</span><span class="sxs-lookup"><span data-stu-id="a7526-114">**ExplorerPolicy**</span></span>](ishelldispatch4-explorerpolicy.md)   | <span data-ttu-id="a7526-115">取得指定 Internet Explorer 原則的值。</span><span class="sxs-lookup"><span data-stu-id="a7526-115">Gets the value for a specified Internet Explorer policy.</span></span><br/> |
| [<span data-ttu-id="a7526-116">**GetSetting**</span><span class="sxs-lookup"><span data-stu-id="a7526-116">**GetSetting**</span></span>](ishelldispatch4-getsetting.md)           | <span data-ttu-id="a7526-117">捕獲全域 Shell 設定。</span><span class="sxs-lookup"><span data-stu-id="a7526-117">Retrieves a global Shell setting.</span></span><br/>                        |
| [<span data-ttu-id="a7526-118">**ToggleDesktop**</span><span class="sxs-lookup"><span data-stu-id="a7526-118">**ToggleDesktop**</span></span>](ishelldispatch4-toggledesktop.md)     | <span data-ttu-id="a7526-119">顯示或隱藏桌面。</span><span class="sxs-lookup"><span data-stu-id="a7526-119">Displays or hides the desktop.</span></span><br/>                           |
| [<span data-ttu-id="a7526-120">**WindowsSecurity**</span><span class="sxs-lookup"><span data-stu-id="a7526-120">**WindowsSecurity**</span></span>](ishelldispatch4-windowssecurity.md) | <span data-ttu-id="a7526-121">顯示 [ **Windows 安全性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a7526-121">Displays the **Windows Security** dialog box.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="a7526-122">備註</span><span class="sxs-lookup"><span data-stu-id="a7526-122">Remarks</span></span>

<span data-ttu-id="a7526-123">如需 Windows 服務的討論，請參閱 [服務](../services/services.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="a7526-123">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7526-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7526-124">Requirements</span></span>



| <span data-ttu-id="a7526-125">需求</span><span class="sxs-lookup"><span data-stu-id="a7526-125">Requirement</span></span> | <span data-ttu-id="a7526-126">值</span><span class="sxs-lookup"><span data-stu-id="a7526-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7526-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7526-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a7526-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7526-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="a7526-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7526-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a7526-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7526-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a7526-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a7526-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7526-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7526-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a7526-133">Idl</span><span class="sxs-lookup"><span data-stu-id="a7526-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7526-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7526-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a7526-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a7526-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7526-136"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a7526-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7526-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7526-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7526-138">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a7526-138">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="a7526-139">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="a7526-139">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="a7526-140">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="a7526-140">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="a7526-141">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="a7526-141">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="a7526-142">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="a7526-142">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> </dl>

 

 
