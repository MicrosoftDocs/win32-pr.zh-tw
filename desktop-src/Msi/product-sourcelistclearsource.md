---
description: SourceListClearSource 方法會移除網路或 URL 來源。 接受型別、來源型別和 SourcePath （來源路徑）作為要移除的參數。 這個方法會呼叫 MsiSourceListClearSource。
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: SourceListClearSource 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993990"
---
# <a name="productsourcelistclearsource-method"></a><span data-ttu-id="a4bdf-105">SourceListClearSource 方法</span><span class="sxs-lookup"><span data-stu-id="a4bdf-105">Product.SourceListClearSource method</span></span>

<span data-ttu-id="a4bdf-106">**SourceListClearSource** 方法會移除網路或 URL 來源。</span><span class="sxs-lookup"><span data-stu-id="a4bdf-106">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="a4bdf-107">接受 *型* 別、來源型別和 *SourcePath*（來源路徑）作為要移除的參數。</span><span class="sxs-lookup"><span data-stu-id="a4bdf-107">Accepts *Type*, the source type, and *SourcePath*, the source path, as parameters to be removed.</span></span> <span data-ttu-id="a4bdf-108">這個方法會呼叫 [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)。</span><span class="sxs-lookup"><span data-stu-id="a4bdf-108">This method calls the [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bdf-109">語法</span><span class="sxs-lookup"><span data-stu-id="a4bdf-109">Syntax</span></span>


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="a4bdf-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4bdf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4bdf-111">*型別*</span><span class="sxs-lookup"><span data-stu-id="a4bdf-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="a4bdf-112">要移除的來源類型： MSISOURCETYPE \_ NETWORK 或 MSISOURCETYPE \_ URL。</span><span class="sxs-lookup"><span data-stu-id="a4bdf-112">Type of source to be removed: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="a4bdf-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="a4bdf-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="a4bdf-114">要移除之來源的路徑。</span><span class="sxs-lookup"><span data-stu-id="a4bdf-114">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4bdf-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4bdf-115">Return value</span></span>

<span data-ttu-id="a4bdf-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a4bdf-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4bdf-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4bdf-117">Requirements</span></span>



| <span data-ttu-id="a4bdf-118">需求</span><span class="sxs-lookup"><span data-stu-id="a4bdf-118">Requirement</span></span> | <span data-ttu-id="a4bdf-119">值</span><span class="sxs-lookup"><span data-stu-id="a4bdf-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4bdf-120">版本</span><span class="sxs-lookup"><span data-stu-id="a4bdf-120">Version</span></span><br/> | <span data-ttu-id="a4bdf-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a4bdf-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a4bdf-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a4bdf-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a4bdf-123">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a4bdf-123">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a4bdf-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a4bdf-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4bdf-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4bdf-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a4bdf-126">IID</span><span class="sxs-lookup"><span data-stu-id="a4bdf-126">IID</span></span><br/>     | <span data-ttu-id="a4bdf-127">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a4bdf-127">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="a4bdf-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4bdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4bdf-129">**產品**</span><span class="sxs-lookup"><span data-stu-id="a4bdf-129">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="a4bdf-130">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="a4bdf-130">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="a4bdf-131">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="a4bdf-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




