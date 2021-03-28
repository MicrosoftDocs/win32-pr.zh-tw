---
description: 擴充 IShellDispatch2 物件。
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: 'IShellDispatch3 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972376"
---
# <a name="ishelldispatch3-object"></a><span data-ttu-id="26c82-103">IShellDispatch3 物件</span><span class="sxs-lookup"><span data-stu-id="26c82-103">IShellDispatch3 object</span></span>

<span data-ttu-id="26c82-104">擴充 [**IShellDispatch2**](ishelldispatch2-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="26c82-104">Extends the [**IShellDispatch2**](ishelldispatch2-object.md) object.</span></span> <span data-ttu-id="26c82-105">除了 **IShellDispatch2** 支援的屬性和方法之外， **IShellDispatch3** 還支援一個新的方法。</span><span class="sxs-lookup"><span data-stu-id="26c82-105">**IShellDispatch3** supports one new method in addition to the properties and methods supported by **IShellDispatch2**.</span></span>

> [!Note]  
> <span data-ttu-id="26c82-106">**IShellDispatch3** 是透過 [**Shell**](shell.md) 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="26c82-106">**IShellDispatch3** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="26c82-107">成員</span><span class="sxs-lookup"><span data-stu-id="26c82-107">Members</span></span>

<span data-ttu-id="26c82-108">**IShellDispatch3** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="26c82-108">The **IShellDispatch3** object has these types of members:</span></span>

-   [<span data-ttu-id="26c82-109">方法</span><span class="sxs-lookup"><span data-stu-id="26c82-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="26c82-110">方法</span><span class="sxs-lookup"><span data-stu-id="26c82-110">Methods</span></span>

<span data-ttu-id="26c82-111">**IShellDispatch3** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="26c82-111">The **IShellDispatch3** object has these methods.</span></span>



| <span data-ttu-id="26c82-112">方法</span><span class="sxs-lookup"><span data-stu-id="26c82-112">Method</span></span>                                             | <span data-ttu-id="26c82-113">描述</span><span class="sxs-lookup"><span data-stu-id="26c82-113">Description</span></span>                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="26c82-114">**AddToRecent**</span><span class="sxs-lookup"><span data-stu-id="26c82-114">**AddToRecent**</span></span>](ishelldispatch3-addtorecent.md) | <span data-ttu-id="26c82-115">將檔案加入最近使用的 (MRU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="26c82-115">Adds a file to the most recently used (MRU) list.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="26c82-116">備註</span><span class="sxs-lookup"><span data-stu-id="26c82-116">Remarks</span></span>

<span data-ttu-id="26c82-117">如需 Windows 服務的討論，請參閱 [服務](../services/services.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="26c82-117">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="26c82-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="26c82-118">Requirements</span></span>



| <span data-ttu-id="26c82-119">需求</span><span class="sxs-lookup"><span data-stu-id="26c82-119">Requirement</span></span> | <span data-ttu-id="26c82-120">值</span><span class="sxs-lookup"><span data-stu-id="26c82-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26c82-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26c82-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26c82-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26c82-122">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="26c82-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26c82-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26c82-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26c82-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="26c82-125">標頭</span><span class="sxs-lookup"><span data-stu-id="26c82-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26c82-126"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="26c82-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="26c82-127">Idl</span><span class="sxs-lookup"><span data-stu-id="26c82-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26c82-128"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="26c82-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="26c82-129">DLL</span><span class="sxs-lookup"><span data-stu-id="26c82-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26c82-130"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="26c82-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26c82-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26c82-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c82-132">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="26c82-132">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="26c82-133">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="26c82-133">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="26c82-134">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="26c82-134">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="26c82-135">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="26c82-135">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> </dl>

 

 
