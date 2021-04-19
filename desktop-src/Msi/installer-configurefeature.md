---
description: 安裝程式物件的 ConfigureFeature 方法會設定產品功能的已安裝狀態。
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.ConfigureFeature 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994913"
---
# <a name="installerconfigurefeature-method"></a><span data-ttu-id="e5dae-103">Installer.ConfigureFeature 方法</span><span class="sxs-lookup"><span data-stu-id="e5dae-103">Installer.ConfigureFeature method</span></span>

<span data-ttu-id="e5dae-104">[**安裝程式**](installer-object.md)物件的 **ConfigureFeature** 方法會設定產品功能的已安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="e5dae-104">The **ConfigureFeature** method of the [**Installer**](installer-object.md) object configures the installed state of a product feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5dae-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5dae-105">Syntax</span></span>


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="e5dae-106">參數</span><span class="sxs-lookup"><span data-stu-id="e5dae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5dae-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="e5dae-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="e5dae-108">指定產品的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="e5dae-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="e5dae-109">*功能*</span><span class="sxs-lookup"><span data-stu-id="e5dae-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="e5dae-110">指定要設定之功能的功能識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5dae-110">Specifies the feature ID of the feature to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="e5dae-111">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="e5dae-111">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="e5dae-112">指定功能的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="e5dae-112">Specifies the installation state for the feature.</span></span> <span data-ttu-id="e5dae-113">此參數必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="e5dae-113">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="e5dae-114">值</span><span class="sxs-lookup"><span data-stu-id="e5dae-114">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="e5dae-115">意義</span><span class="sxs-lookup"><span data-stu-id="e5dae-115">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="e5dae-116"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="e5dae-116"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="e5dae-117">此功能已公告</span><span class="sxs-lookup"><span data-stu-id="e5dae-117">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="e5dae-118"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="e5dae-118"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="e5dae-119">這項功能會安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="e5dae-119">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="e5dae-120"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="e5dae-120"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="e5dae-121">這項功能已卸載。</span><span class="sxs-lookup"><span data-stu-id="e5dae-121">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="e5dae-122"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="e5dae-122"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="e5dae-123">這項功能已安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="e5dae-123">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="e5dae-124"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="e5dae-124"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="e5dae-125">這項功能會安裝到其預設位置。</span><span class="sxs-lookup"><span data-stu-id="e5dae-125">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5dae-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5dae-126">Return value</span></span>

<span data-ttu-id="e5dae-127">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e5dae-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5dae-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5dae-128">Requirements</span></span>



| <span data-ttu-id="e5dae-129">需求</span><span class="sxs-lookup"><span data-stu-id="e5dae-129">Requirement</span></span> | <span data-ttu-id="e5dae-130">值</span><span class="sxs-lookup"><span data-stu-id="e5dae-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5dae-131">版本</span><span class="sxs-lookup"><span data-stu-id="e5dae-131">Version</span></span><br/> | <span data-ttu-id="e5dae-132">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e5dae-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e5dae-133">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e5dae-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e5dae-134">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e5dae-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e5dae-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e5dae-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5dae-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5dae-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e5dae-137">IID</span><span class="sxs-lookup"><span data-stu-id="e5dae-137">IID</span></span><br/>     | <span data-ttu-id="e5dae-138">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e5dae-138">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e5dae-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5dae-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5dae-140">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="e5dae-140">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[<span data-ttu-id="e5dae-141">安裝和設定功能</span><span class="sxs-lookup"><span data-stu-id="e5dae-141">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




