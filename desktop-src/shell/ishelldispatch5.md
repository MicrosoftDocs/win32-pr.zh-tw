---
description: 擴充 IShellDispatch4 物件。
title: 'IShellDispatch5 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842999"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="ee1f7-103">IShellDispatch5 物件</span><span class="sxs-lookup"><span data-stu-id="ee1f7-103">IShellDispatch5 object</span></span>

<span data-ttu-id="ee1f7-104">擴充 [**IShellDispatch4**](ishelldispatch4.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ee1f7-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="ee1f7-105">除了 **IShellDispatch4** 所支援的屬性和方法之外， **IShellDispatch5** 還新增了在3d 堆疊中顯示開啟視窗的方法。</span><span class="sxs-lookup"><span data-stu-id="ee1f7-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="ee1f7-106">**IShellDispatch5** 是透過 [**Shell**](shell.md) 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="ee1f7-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="ee1f7-107">成員</span><span class="sxs-lookup"><span data-stu-id="ee1f7-107">Members</span></span>

<span data-ttu-id="ee1f7-108">**IShellDispatch5** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ee1f7-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="ee1f7-109">方法</span><span class="sxs-lookup"><span data-stu-id="ee1f7-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ee1f7-110">方法</span><span class="sxs-lookup"><span data-stu-id="ee1f7-110">Methods</span></span>

<span data-ttu-id="ee1f7-111">**IShellDispatch5** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ee1f7-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="ee1f7-112">方法</span><span class="sxs-lookup"><span data-stu-id="ee1f7-112">Method</span></span>                                                   | <span data-ttu-id="ee1f7-113">描述</span><span class="sxs-lookup"><span data-stu-id="ee1f7-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="ee1f7-114">**WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="ee1f7-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="ee1f7-115">將開啟的視窗顯示在您可以切換的3D 堆疊中。</span><span class="sxs-lookup"><span data-stu-id="ee1f7-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ee1f7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee1f7-116">Requirements</span></span>



| <span data-ttu-id="ee1f7-117">需求</span><span class="sxs-lookup"><span data-stu-id="ee1f7-117">Requirement</span></span> | <span data-ttu-id="ee1f7-118">值</span><span class="sxs-lookup"><span data-stu-id="ee1f7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1f7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee1f7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee1f7-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee1f7-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ee1f7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee1f7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee1f7-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee1f7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ee1f7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ee1f7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee1f7-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee1f7-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ee1f7-125">Idl</span><span class="sxs-lookup"><span data-stu-id="ee1f7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee1f7-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee1f7-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ee1f7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ee1f7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee1f7-128"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="ee1f7-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee1f7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee1f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1f7-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ee1f7-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="ee1f7-131">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="ee1f7-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="ee1f7-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="ee1f7-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="ee1f7-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="ee1f7-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="ee1f7-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="ee1f7-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="ee1f7-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="ee1f7-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
