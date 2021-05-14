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
ms.openlocfilehash: daec9c922a0bac05154c1108f236ddf336a2e380
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843059"
---
# <a name="ishelldispatch4-object"></a><span data-ttu-id="a9f7d-103">IShellDispatch4 物件</span><span class="sxs-lookup"><span data-stu-id="a9f7d-103">IShellDispatch4 object</span></span>

<span data-ttu-id="a9f7d-104">擴充 [**IShellDispatch3**](ishelldispatch3.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-104">Extends the [**IShellDispatch3**](ishelldispatch3.md) object.</span></span> <span data-ttu-id="a9f7d-105">除了 **IShellDispatch3** 支援的屬性和方法之外， **IShellDispatch4** 還支援四個額外的方法。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-105">In addition to the properties and methods supported by **IShellDispatch3**, **IShellDispatch4** supports four additional methods.</span></span>

> [!Note]  
> <span data-ttu-id="a9f7d-106">**IShellDispatch4** 是透過 [**Shell**](shell.md) 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-106">**IShellDispatch4** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="a9f7d-107">成員</span><span class="sxs-lookup"><span data-stu-id="a9f7d-107">Members</span></span>

<span data-ttu-id="a9f7d-108">**IShellDispatch4** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a9f7d-108">The **IShellDispatch4** object has these types of members:</span></span>

-   [<span data-ttu-id="a9f7d-109">方法</span><span class="sxs-lookup"><span data-stu-id="a9f7d-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9f7d-110">方法</span><span class="sxs-lookup"><span data-stu-id="a9f7d-110">Methods</span></span>

<span data-ttu-id="a9f7d-111">**IShellDispatch4** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-111">The **IShellDispatch4** object has these methods.</span></span>



| <span data-ttu-id="a9f7d-112">方法</span><span class="sxs-lookup"><span data-stu-id="a9f7d-112">Method</span></span>                                                     | <span data-ttu-id="a9f7d-113">描述</span><span class="sxs-lookup"><span data-stu-id="a9f7d-113">Description</span></span>                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="a9f7d-114">**ExplorerPolicy**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-114">**ExplorerPolicy**</span></span>](ishelldispatch4-explorerpolicy.md)   | <span data-ttu-id="a9f7d-115">取得指定 Internet Explorer 原則的值。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-115">Gets the value for a specified Internet Explorer policy.</span></span><br/> |
| [<span data-ttu-id="a9f7d-116">**GetSetting**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-116">**GetSetting**</span></span>](ishelldispatch4-getsetting.md)           | <span data-ttu-id="a9f7d-117">捕獲全域 Shell 設定。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-117">Retrieves a global Shell setting.</span></span><br/>                        |
| [<span data-ttu-id="a9f7d-118">**ToggleDesktop**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-118">**ToggleDesktop**</span></span>](ishelldispatch4-toggledesktop.md)     | <span data-ttu-id="a9f7d-119">顯示或隱藏桌面。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-119">Displays or hides the desktop.</span></span><br/>                           |
| [<span data-ttu-id="a9f7d-120">**WindowsSecurity**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-120">**WindowsSecurity**</span></span>](ishelldispatch4-windowssecurity.md) | <span data-ttu-id="a9f7d-121">顯示 [ **Windows 安全性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-121">Displays the **Windows Security** dialog box.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="a9f7d-122">備註</span><span class="sxs-lookup"><span data-stu-id="a9f7d-122">Remarks</span></span>

<span data-ttu-id="a9f7d-123">如需 Windows 服務的討論，請參閱 [服務](../services/services.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="a9f7d-123">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9f7d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9f7d-124">Requirements</span></span>



| <span data-ttu-id="a9f7d-125">需求</span><span class="sxs-lookup"><span data-stu-id="a9f7d-125">Requirement</span></span> | <span data-ttu-id="a9f7d-126">值</span><span class="sxs-lookup"><span data-stu-id="a9f7d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f7d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9f7d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a9f7d-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9f7d-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="a9f7d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9f7d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a9f7d-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9f7d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a9f7d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a9f7d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9f7d-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f7d-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a9f7d-133">Idl</span><span class="sxs-lookup"><span data-stu-id="a9f7d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9f7d-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9f7d-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a9f7d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a9f7d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9f7d-136"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a9f7d-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9f7d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9f7d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f7d-138">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-138">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="a9f7d-139">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-139">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="a9f7d-140">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-140">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="a9f7d-141">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-141">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="a9f7d-142">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="a9f7d-142">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> </dl>

 

 
