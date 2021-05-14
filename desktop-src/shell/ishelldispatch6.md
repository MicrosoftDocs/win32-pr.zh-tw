---
description: 擴充 IShellDispatch5 物件。
title: 'IShellDispatch6 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch6
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.openlocfilehash: de27322324dc8a25bdc679374e625f94a1d1a2ae
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843029"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="57b09-103">IShellDispatch6 物件</span><span class="sxs-lookup"><span data-stu-id="57b09-103">IShellDispatch6 object</span></span>

<span data-ttu-id="57b09-104">擴充 [**IShellDispatch5**](ishelldispatch5.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="57b09-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="57b09-105">除了 **IShellDispatch5** 支援的屬性和方法之外， **IShellDispatch6** 也會新增可顯示應用程式搜尋窗格的方法。</span><span class="sxs-lookup"><span data-stu-id="57b09-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="57b09-106">**IShellDispatch6** 是透過 [**Shell**](shell.md) 物件來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="57b09-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="57b09-107">成員</span><span class="sxs-lookup"><span data-stu-id="57b09-107">Members</span></span>

<span data-ttu-id="57b09-108">**IShellDispatch6** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="57b09-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="57b09-109">方法</span><span class="sxs-lookup"><span data-stu-id="57b09-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="57b09-110">方法</span><span class="sxs-lookup"><span data-stu-id="57b09-110">Methods</span></span>

<span data-ttu-id="57b09-111">**IShellDispatch6** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="57b09-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="57b09-112">方法</span><span class="sxs-lookup"><span data-stu-id="57b09-112">Method</span></span>                                                 | <span data-ttu-id="57b09-113">描述</span><span class="sxs-lookup"><span data-stu-id="57b09-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57b09-114">**SearchCommand**</span><span class="sxs-lookup"><span data-stu-id="57b09-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="57b09-115">顯示應用程式搜尋窗格，通常會在您開始從開始畫面輸入搜尋字詞時出現。</span><span class="sxs-lookup"><span data-stu-id="57b09-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="57b09-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="57b09-116">Requirements</span></span>



| <span data-ttu-id="57b09-117">需求</span><span class="sxs-lookup"><span data-stu-id="57b09-117">Requirement</span></span> | <span data-ttu-id="57b09-118">值</span><span class="sxs-lookup"><span data-stu-id="57b09-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57b09-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57b09-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57b09-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57b09-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="57b09-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57b09-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57b09-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57b09-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="57b09-123">標頭</span><span class="sxs-lookup"><span data-stu-id="57b09-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b09-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="57b09-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="57b09-125">Idl</span><span class="sxs-lookup"><span data-stu-id="57b09-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57b09-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="57b09-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="57b09-127">DLL</span><span class="sxs-lookup"><span data-stu-id="57b09-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57b09-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57b09-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b09-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57b09-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b09-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="57b09-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="57b09-131">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="57b09-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="57b09-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="57b09-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="57b09-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="57b09-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="57b09-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="57b09-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="57b09-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="57b09-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="57b09-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="57b09-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 
