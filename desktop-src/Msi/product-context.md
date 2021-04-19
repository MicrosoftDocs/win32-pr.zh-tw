---
description: CoNtext 屬性會傳回此產品的內容。
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Product. CoNtext 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8334ca57d552681afeb77d0b213eca8b92bc1234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999620"
---
# <a name="productcontext-property"></a><span data-ttu-id="45b85-103">Product. CoNtext 屬性</span><span class="sxs-lookup"><span data-stu-id="45b85-103">Product.Context property</span></span>

<span data-ttu-id="45b85-104">**CoNtext** 屬性會傳回此產品的內容。</span><span class="sxs-lookup"><span data-stu-id="45b85-104">The **Context** property returns the context of this product.</span></span>

<span data-ttu-id="45b85-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="45b85-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b85-106">語法</span><span class="sxs-lookup"><span data-stu-id="45b85-106">Syntax</span></span>


```JScript
propVal = Product.Context
```



## <a name="property-value"></a><span data-ttu-id="45b85-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="45b85-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="45b85-108">備註</span><span class="sxs-lookup"><span data-stu-id="45b85-108">Remarks</span></span>

<span data-ttu-id="45b85-109">這個屬性可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="45b85-109">This property can return one of the following values.</span></span>



| <span data-ttu-id="45b85-110">Context</span><span class="sxs-lookup"><span data-stu-id="45b85-110">Context</span></span>                        | <span data-ttu-id="45b85-111">值</span><span class="sxs-lookup"><span data-stu-id="45b85-111">Value</span></span> | <span data-ttu-id="45b85-112">意義</span><span class="sxs-lookup"><span data-stu-id="45b85-112">Meaning</span></span>                           |
|--------------------------------|-------|-----------------------------------|
| <span data-ttu-id="45b85-113">MSIINSTALLCONTEXT \_ USERMANAGED</span><span class="sxs-lookup"><span data-stu-id="45b85-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="45b85-114">1</span><span class="sxs-lookup"><span data-stu-id="45b85-114">1</span></span>     | <span data-ttu-id="45b85-115">受管理內容下的產品。</span><span class="sxs-lookup"><span data-stu-id="45b85-115">Products under managed context.</span></span>   |
| <span data-ttu-id="45b85-116">MSIINSTALLCONTEXT \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="45b85-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="45b85-117">2</span><span class="sxs-lookup"><span data-stu-id="45b85-117">2</span></span>     | <span data-ttu-id="45b85-118">非受控內容下的產品。</span><span class="sxs-lookup"><span data-stu-id="45b85-118">Products under unmanaged context.</span></span> |
| <span data-ttu-id="45b85-119">MSIINSTALLCONTEXT \_ 機器</span><span class="sxs-lookup"><span data-stu-id="45b85-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="45b85-120">4</span><span class="sxs-lookup"><span data-stu-id="45b85-120">4</span></span>     | <span data-ttu-id="45b85-121">電腦內容下的產品。</span><span class="sxs-lookup"><span data-stu-id="45b85-121">Products under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="45b85-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="45b85-122">Requirements</span></span>



| <span data-ttu-id="45b85-123">需求</span><span class="sxs-lookup"><span data-stu-id="45b85-123">Requirement</span></span> | <span data-ttu-id="45b85-124">值</span><span class="sxs-lookup"><span data-stu-id="45b85-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b85-125">版本</span><span class="sxs-lookup"><span data-stu-id="45b85-125">Version</span></span><br/> | <span data-ttu-id="45b85-126">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="45b85-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="45b85-127">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="45b85-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="45b85-128">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="45b85-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="45b85-129">DLL</span><span class="sxs-lookup"><span data-stu-id="45b85-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="45b85-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b85-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="45b85-131">IID</span><span class="sxs-lookup"><span data-stu-id="45b85-131">IID</span></span><br/>     | <span data-ttu-id="45b85-132">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="45b85-132">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="45b85-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45b85-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b85-134">**產品**</span><span class="sxs-lookup"><span data-stu-id="45b85-134">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="45b85-135">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="45b85-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




