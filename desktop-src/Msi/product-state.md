---
description: State 屬性會傳回這個產品實例的安裝狀態。
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Product. State 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993573"
---
# <a name="productstate-property"></a><span data-ttu-id="4829c-103">Product. State 屬性</span><span class="sxs-lookup"><span data-stu-id="4829c-103">Product.State property</span></span>

<span data-ttu-id="4829c-104">**State** 屬性會傳回這個產品實例的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="4829c-104">The **State** property returns the installation state of this instance of the product.</span></span>

<span data-ttu-id="4829c-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4829c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4829c-106">語法</span><span class="sxs-lookup"><span data-stu-id="4829c-106">Syntax</span></span>


```JScript
propVal = Product.State
```



## <a name="property-value"></a><span data-ttu-id="4829c-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="4829c-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="4829c-108">備註</span><span class="sxs-lookup"><span data-stu-id="4829c-108">Remarks</span></span>

<span data-ttu-id="4829c-109">這個屬性會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4829c-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="4829c-110">安裝狀態</span><span class="sxs-lookup"><span data-stu-id="4829c-110">Installation State</span></span>       | <span data-ttu-id="4829c-111">意義</span><span class="sxs-lookup"><span data-stu-id="4829c-111">Meaning</span></span>                                |
|--------------------------|----------------------------------------|
| <span data-ttu-id="4829c-112">INSTALLSTATE \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="4829c-112">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="4829c-113">在本機安裝之產品的實例。</span><span class="sxs-lookup"><span data-stu-id="4829c-113">Instance of product installed locally.</span></span> |
| <span data-ttu-id="4829c-114">INSTALLSTATE \_ 公告</span><span class="sxs-lookup"><span data-stu-id="4829c-114">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="4829c-115">已公告產品的實例。</span><span class="sxs-lookup"><span data-stu-id="4829c-115">Instance of product advertised.</span></span>        |
| <span data-ttu-id="4829c-116">INSTALLSTATE \_ 不明</span><span class="sxs-lookup"><span data-stu-id="4829c-116">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="4829c-117">未知產品的實例。</span><span class="sxs-lookup"><span data-stu-id="4829c-117">Instance of product unknown.</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="4829c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4829c-118">Requirements</span></span>



| <span data-ttu-id="4829c-119">需求</span><span class="sxs-lookup"><span data-stu-id="4829c-119">Requirement</span></span> | <span data-ttu-id="4829c-120">值</span><span class="sxs-lookup"><span data-stu-id="4829c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4829c-121">版本</span><span class="sxs-lookup"><span data-stu-id="4829c-121">Version</span></span><br/> | <span data-ttu-id="4829c-122">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4829c-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4829c-123">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4829c-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4829c-124">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4829c-124">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="4829c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4829c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4829c-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4829c-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="4829c-127">IID</span><span class="sxs-lookup"><span data-stu-id="4829c-127">IID</span></span><br/>     | <span data-ttu-id="4829c-128">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4829c-128">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="4829c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4829c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4829c-130">**產品**</span><span class="sxs-lookup"><span data-stu-id="4829c-130">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="4829c-131">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="4829c-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




