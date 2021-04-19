---
description: ApplyMultiplePatches 方法會將一或多個修補程式套用至有資格接收修補程式的產品。 方法會設定 PATCH 屬性。
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: ApplyMultiplePatches 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993355"
---
# <a name="installerapplymultiplepatches-method"></a><span data-ttu-id="c526d-104">ApplyMultiplePatches 方法</span><span class="sxs-lookup"><span data-stu-id="c526d-104">Installer.ApplyMultiplePatches method</span></span>

<span data-ttu-id="c526d-105">**ApplyMultiplePatches** 方法會將一或多個修補程式套用至有資格接收修補程式的產品。</span><span class="sxs-lookup"><span data-stu-id="c526d-105">The **ApplyMultiplePatches** method applies one or more patches to products that are eligible to receive the patch.</span></span> <span data-ttu-id="c526d-106">方法會設定 [**PATCH**](patch.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c526d-106">The method sets the [**PATCH**](patch.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c526d-107">語法</span><span class="sxs-lookup"><span data-stu-id="c526d-107">Syntax</span></span>


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a><span data-ttu-id="c526d-108">參數</span><span class="sxs-lookup"><span data-stu-id="c526d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c526d-109">*PatchPackagesList*</span><span class="sxs-lookup"><span data-stu-id="c526d-109">*PatchPackagesList*</span></span> 
</dt> <dd>

<span data-ttu-id="c526d-110">字串，包含要修補檔案之路徑的分號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="c526d-110">A string that contains a semicolon-delimited list of the paths to patch files.</span></span> <span data-ttu-id="c526d-111">例如： "" c： \\ sus 下載快取 \\ \\ \\ Office \\ sp1 .msp;c： \\ sus \\ 下載快取 \\ \\ office \\ QFE1 .msp; c： su 下載快取 \\ \\ \\ \\ office \\ QFEn .msp ""</span><span class="sxs-lookup"><span data-stu-id="c526d-111">For example: ""c:\\sus\\download\\cache\\Office\\sp1.msp; c:\\sus\\download\\cache\\Office\\QFE1.msp;c:\\sus\\download\\cache\\Office\\QFEn.msp""</span></span>

</dd> <dt>

<span data-ttu-id="c526d-112">*產品*</span><span class="sxs-lookup"><span data-stu-id="c526d-112">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="c526d-113">此參數提供所修補產品的 [**ProductCode**](productcode.md) 。</span><span class="sxs-lookup"><span data-stu-id="c526d-113">This parameter provides the [**ProductCode**](productcode.md) of the product being patched.</span></span> <span data-ttu-id="c526d-114">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="c526d-114">This parameter is optional.</span></span> <span data-ttu-id="c526d-115">當此參數為 null 時，會將修補程式套用至有資格接收這些修補程式的所有產品。</span><span class="sxs-lookup"><span data-stu-id="c526d-115">When this parameter is null, the patches are applied to all products that are eligible to receive these patches.</span></span>

</dd> <dt>

<span data-ttu-id="c526d-116">*szPropertiesList*</span><span class="sxs-lookup"><span data-stu-id="c526d-116">*szPropertiesList*</span></span> 
</dt> <dd>

<span data-ttu-id="c526d-117">指定命令列屬性設定的以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="c526d-117">A null-terminated string that specifies command-line property settings.</span></span> <span data-ttu-id="c526d-118">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="c526d-118">This parameter is optional.</span></span> <span data-ttu-id="c526d-119">請參閱 [關於屬性](about-properties.md) ，並 [在命令列上設定公用屬性值](setting-public-property-values-on-the-command-line.md)。</span><span class="sxs-lookup"><span data-stu-id="c526d-119">See [About Properties](about-properties.md) and [Setting Public Property Values on the Command Line](setting-public-property-values-on-the-command-line.md).</span></span> <span data-ttu-id="c526d-120">這些屬性會由所有目標產品共用。</span><span class="sxs-lookup"><span data-stu-id="c526d-120">These properties are shared by all target products.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c526d-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="c526d-121">Return value</span></span>

<span data-ttu-id="c526d-122">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c526d-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c526d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c526d-123">Requirements</span></span>



| <span data-ttu-id="c526d-124">需求</span><span class="sxs-lookup"><span data-stu-id="c526d-124">Requirement</span></span> | <span data-ttu-id="c526d-125">值</span><span class="sxs-lookup"><span data-stu-id="c526d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c526d-126">版本</span><span class="sxs-lookup"><span data-stu-id="c526d-126">Version</span></span><br/> | <span data-ttu-id="c526d-127">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c526d-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c526d-128">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c526d-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c526d-129">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c526d-129">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="c526d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c526d-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="c526d-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c526d-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="c526d-132">IID</span><span class="sxs-lookup"><span data-stu-id="c526d-132">IID</span></span><br/>     | <span data-ttu-id="c526d-133">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c526d-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="c526d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c526d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c526d-135">關於屬性</span><span class="sxs-lookup"><span data-stu-id="c526d-135">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="c526d-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="c526d-136">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="c526d-137">**補丁**</span><span class="sxs-lookup"><span data-stu-id="c526d-137">**PATCH**</span></span>](patch.md)
</dt> <dt>

[<span data-ttu-id="c526d-138">在命令列上設定公用屬性值</span><span class="sxs-lookup"><span data-stu-id="c526d-138">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="c526d-139">**MsiApplyMultiplePatches**</span><span class="sxs-lookup"><span data-stu-id="c526d-139">**MsiApplyMultiplePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[<span data-ttu-id="c526d-140">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="c526d-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




