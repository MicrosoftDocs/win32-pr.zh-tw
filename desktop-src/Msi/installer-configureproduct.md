---
description: 安裝程式物件的 ConfigureProduct 方法會安裝或卸載產品。
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.ConfigureProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993685"
---
# <a name="installerconfigureproduct-method"></a><span data-ttu-id="6782a-103">Installer.ConfigureProduct 方法</span><span class="sxs-lookup"><span data-stu-id="6782a-103">Installer.ConfigureProduct method</span></span>

<span data-ttu-id="6782a-104">[**安裝程式**](installer-object.md)物件的 **ConfigureProduct** 方法會安裝或卸載產品。</span><span class="sxs-lookup"><span data-stu-id="6782a-104">The **ConfigureProduct** method of the [**Installer**](installer-object.md) object installs or uninstalls a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="6782a-105">語法</span><span class="sxs-lookup"><span data-stu-id="6782a-105">Syntax</span></span>


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="6782a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6782a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6782a-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="6782a-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="6782a-108">指定產品的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="6782a-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="6782a-109">*InstallLevel*</span><span class="sxs-lookup"><span data-stu-id="6782a-109">*InstallLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="6782a-110">指定產品的預設安裝設定。</span><span class="sxs-lookup"><span data-stu-id="6782a-110">Specifies the default installation configuration of the product.</span></span> <span data-ttu-id="6782a-111">如果 InstallState 參數設定為 msiInstallStateDefault 以外的任何其他值，則會忽略 InstallLevel 參數，並安裝所有功能。</span><span class="sxs-lookup"><span data-stu-id="6782a-111">The InstallLevel parameter is ignored and all features are installed if the InstallState parameter is set to any other value than msiInstallStateDefault.</span></span>

<span data-ttu-id="6782a-112">此參數必須是 0 (使用撰寫的功能層級進行安裝) 、65535 (安裝所有功能) ，或介於0到65535之間的值，以安裝可用功能的子集。</span><span class="sxs-lookup"><span data-stu-id="6782a-112">This parameter must be either 0 (install using authored feature levels), 65535 (install all features), or a value between 0 and 65535 to install a subset of available features.</span></span>

</dd> <dt>

<span data-ttu-id="6782a-113">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="6782a-113">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="6782a-114">指定功能的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="6782a-114">Specifies the installation state for the feature.</span></span> <span data-ttu-id="6782a-115">此參數必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="6782a-115">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="6782a-116">值</span><span class="sxs-lookup"><span data-stu-id="6782a-116">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="6782a-117">意義</span><span class="sxs-lookup"><span data-stu-id="6782a-117">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="6782a-118"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="6782a-118"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="6782a-119">此功能已公告</span><span class="sxs-lookup"><span data-stu-id="6782a-119">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="6782a-120"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="6782a-120"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="6782a-121">這項功能會安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="6782a-121">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="6782a-122"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="6782a-122"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="6782a-123">這項功能已卸載。</span><span class="sxs-lookup"><span data-stu-id="6782a-123">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="6782a-124"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="6782a-124"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="6782a-125">這項功能已安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="6782a-125">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="6782a-126"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="6782a-126"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="6782a-127">這項功能會安裝到其預設位置。</span><span class="sxs-lookup"><span data-stu-id="6782a-127">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6782a-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="6782a-128">Return value</span></span>

<span data-ttu-id="6782a-129">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6782a-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6782a-130">備註</span><span class="sxs-lookup"><span data-stu-id="6782a-130">Remarks</span></span>

<span data-ttu-id="6782a-131">**ConfigureProduct** 方法會使用目前的設定來顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="6782a-131">The **ConfigureProduct** method displays the user interface using current settings.</span></span> <span data-ttu-id="6782a-132">在呼叫 **ConfigureProduct** 方法之前，您可以藉由修改 [**UILevel 屬性 (安裝程式物件)**](installer-uilevel.md)來變更使用者介面設定。</span><span class="sxs-lookup"><span data-stu-id="6782a-132">User interface settings can be changed by modifying the [**UILevel property (Installer object)**](installer-uilevel.md) before calling the **ConfigureProduct** method.</span></span>

<span data-ttu-id="6782a-133">如果 *InstallState* 參數設定為 msiInstallStateDefault 以外的任何其他值，則會忽略 *InstallLevel* 參數，並安裝產品的所有功能。</span><span class="sxs-lookup"><span data-stu-id="6782a-133">If the *InstallState* parameter is set to any other value than msiInstallStateDefault, the *InstallLevel* parameter is ignored and all features of the product are installed.</span></span> <span data-ttu-id="6782a-134">當 *InstallState* 參數未設定為 msiInstallStateDefault 時，請使用 [**ConfigureFeature**](installer-configurefeature.md)方法來控制個別功能的安裝。</span><span class="sxs-lookup"><span data-stu-id="6782a-134">Use the [**ConfigureFeature**](installer-configurefeature.md) method to control the installation of individual features when the *InstallState* parameter is not set to msiInstallStateDefault.</span></span>

## <a name="requirements"></a><span data-ttu-id="6782a-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="6782a-135">Requirements</span></span>



| <span data-ttu-id="6782a-136">需求</span><span class="sxs-lookup"><span data-stu-id="6782a-136">Requirement</span></span> | <span data-ttu-id="6782a-137">值</span><span class="sxs-lookup"><span data-stu-id="6782a-137">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6782a-138">版本</span><span class="sxs-lookup"><span data-stu-id="6782a-138">Version</span></span><br/> | <span data-ttu-id="6782a-139">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="6782a-139">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6782a-140">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="6782a-140">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6782a-141">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6782a-141">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6782a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6782a-142">DLL</span></span><br/>     | <dl> <span data-ttu-id="6782a-143"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6782a-143"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6782a-144">IID</span><span class="sxs-lookup"><span data-stu-id="6782a-144">IID</span></span><br/>     | <span data-ttu-id="6782a-145">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6782a-145">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="6782a-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6782a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6782a-147">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="6782a-147">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[<span data-ttu-id="6782a-148">安裝和設定功能</span><span class="sxs-lookup"><span data-stu-id="6782a-148">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




