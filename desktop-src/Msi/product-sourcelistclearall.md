---
description: SourceListClearAll 方法，Product 物件會移除產品的所有來源。 您可以指定要移除的來源型別。
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: SourceListClearAll 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995218"
---
# <a name="productsourcelistclearall-method"></a><span data-ttu-id="3b90d-104">SourceListClearAll 方法</span><span class="sxs-lookup"><span data-stu-id="3b90d-104">Product.SourceListClearAll method</span></span>

<span data-ttu-id="3b90d-105">**SourceListClearAll** 方法， [**product**](product-object.md)物件會移除產品的所有來源。</span><span class="sxs-lookup"><span data-stu-id="3b90d-105">The **SourceListClearAll** method the [**Product**](product-object.md) object removes all sources for the product.</span></span> <span data-ttu-id="3b90d-106">您可以指定要移除的來源型別。</span><span class="sxs-lookup"><span data-stu-id="3b90d-106">The type of source to remove can be specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b90d-107">語法</span><span class="sxs-lookup"><span data-stu-id="3b90d-107">Syntax</span></span>


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="3b90d-108">參數</span><span class="sxs-lookup"><span data-stu-id="3b90d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b90d-109">*型別*</span><span class="sxs-lookup"><span data-stu-id="3b90d-109">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="3b90d-110">要移除的來源類型： MSISOURCETYPE \_ MEDIA、MSISOURCETYPE \_ NETWORK 或 MSISOURCETYPE \_ URL。</span><span class="sxs-lookup"><span data-stu-id="3b90d-110">Type of source to be removed: MSISOURCETYPE\_MEDIA, MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b90d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b90d-111">Return value</span></span>

<span data-ttu-id="3b90d-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3b90d-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b90d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b90d-113">Requirements</span></span>



| <span data-ttu-id="3b90d-114">需求</span><span class="sxs-lookup"><span data-stu-id="3b90d-114">Requirement</span></span> | <span data-ttu-id="3b90d-115">值</span><span class="sxs-lookup"><span data-stu-id="3b90d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b90d-116">版本</span><span class="sxs-lookup"><span data-stu-id="3b90d-116">Version</span></span><br/> | <span data-ttu-id="3b90d-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="3b90d-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3b90d-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="3b90d-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3b90d-119">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3b90d-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="3b90d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3b90d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b90d-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b90d-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="3b90d-122">IID</span><span class="sxs-lookup"><span data-stu-id="3b90d-122">IID</span></span><br/>     | <span data-ttu-id="3b90d-123">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3b90d-123">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="3b90d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b90d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b90d-125">**產品**</span><span class="sxs-lookup"><span data-stu-id="3b90d-125">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="3b90d-126">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="3b90d-126">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="3b90d-127">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="3b90d-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




