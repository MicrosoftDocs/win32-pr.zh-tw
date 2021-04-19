---
description: 針對 patch 套件所列出的每項產品，都有資格接收修補程式，安裝程式物件的 ApplyPatch 方法會叫用安裝，並將 PATCH 屬性設定為 patch 封裝的路徑。
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: ApplyPatch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982617"
---
# <a name="installerapplypatch-method"></a><span data-ttu-id="38f1d-103">ApplyPatch 方法</span><span class="sxs-lookup"><span data-stu-id="38f1d-103">Installer.ApplyPatch method</span></span>

<span data-ttu-id="38f1d-104">針對 patch 套件所列出的每項產品，都有資格接收修補程式，[**安裝程式**](installer-object.md)物件的 **ApplyPatch** 方法會叫用安裝，並將 [**patch**](patch.md)屬性設定為 patch 封裝的路徑。</span><span class="sxs-lookup"><span data-stu-id="38f1d-104">For each product listed by the patch package as eligible to receive the patch, the **ApplyPatch** method of the [**Installer**](installer-object.md) object invokes an installation and sets the [**PATCH**](patch.md) property to the path of the patch package.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f1d-105">語法</span><span class="sxs-lookup"><span data-stu-id="38f1d-105">Syntax</span></span>


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a><span data-ttu-id="38f1d-106">參數</span><span class="sxs-lookup"><span data-stu-id="38f1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f1d-107">*PatchPackage*</span><span class="sxs-lookup"><span data-stu-id="38f1d-107">*PatchPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="38f1d-108">指定修補封裝的路徑。</span><span class="sxs-lookup"><span data-stu-id="38f1d-108">Specifies a path to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="38f1d-109">*InstallPackage*</span><span class="sxs-lookup"><span data-stu-id="38f1d-109">*InstallPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="38f1d-110">如果 *InstallType* 設定為 msiInstallTypeNetworkImage，則 *InstallPackage* 會指定要修補的產品路徑。</span><span class="sxs-lookup"><span data-stu-id="38f1d-110">If *InstallType* is set to msiInstallTypeNetworkImage, *InstallPackage* specifies the path to the product that is to be patched.</span></span> <span data-ttu-id="38f1d-111">如果 *InstallType* 設定為 msiInstallTypeDefault，且 *InstallPackage* 設定為0，則安裝程式會將修補程式套用至修補套件中所列的每個合格產品。</span><span class="sxs-lookup"><span data-stu-id="38f1d-111">If *InstallType* is set to msiInstallTypeDefault and *InstallPackage* is set to 0, the installer applies the patch to every eligible product listed in the patch package.</span></span>

<span data-ttu-id="38f1d-112">如果 *InstallType* 是 msiInstallTypeSingleInstance，則安裝程式會將修補程式套用至 *InstallPackage* 所指定的產品。</span><span class="sxs-lookup"><span data-stu-id="38f1d-112">If *InstallType* is msiInstallTypeSingleInstance, the installer applies the patch to the product specified by *InstallPackage*.</span></span> <span data-ttu-id="38f1d-113">在此情況下，會忽略 patch 套件中所列的其他合格產品，且 *InstallPackage* 參數會包含以 null 終止的字串，代表要修補之實例的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="38f1d-113">In this case, other eligible products listed in the patch package are ignored and the *InstallPackage* parameter contains the null-terminated string representing the product code of the instance to patch.</span></span> <span data-ttu-id="38f1d-114">這種類型的安裝需要 Windows Server 2003 或更新版本所隨附的 Windows Installer 版本，或是 Windows Installer XP SP1 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="38f1d-114">This type of installation requires the Windows Installer version shipped with the Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span>

</dd> <dt>

<span data-ttu-id="38f1d-115">*InstallType*</span><span class="sxs-lookup"><span data-stu-id="38f1d-115">*InstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="38f1d-116">此參數會指定要修補的安裝類型。</span><span class="sxs-lookup"><span data-stu-id="38f1d-116">This parameter specifies the type of installation to patch.</span></span> <span data-ttu-id="38f1d-117">如果省略 *InstallPackage* ，則會忽略 *InstallType* 參數。</span><span class="sxs-lookup"><span data-stu-id="38f1d-117">The *InstallType* parameter is ignored if *InstallPackage* is omitted.</span></span>



| <span data-ttu-id="38f1d-118">值</span><span class="sxs-lookup"><span data-stu-id="38f1d-118">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="38f1d-119">意義</span><span class="sxs-lookup"><span data-stu-id="38f1d-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <span data-ttu-id="38f1d-120"><dt>**msiInstallTypeNetworkImage**</dt></span><span class="sxs-lookup"><span data-stu-id="38f1d-120"><dt>**msiInstallTypeNetworkImage**</dt></span></span> </dl> | <span data-ttu-id="38f1d-121">表示系統管理安裝。</span><span class="sxs-lookup"><span data-stu-id="38f1d-121">Indicates a administrative installation.</span></span> <span data-ttu-id="38f1d-122">在此情況下， *InstallPackage* 必須設定為封裝路徑。</span><span class="sxs-lookup"><span data-stu-id="38f1d-122">In this case, *InstallPackage* must be set to a package path.</span></span> <span data-ttu-id="38f1d-123">MsiInstallTypeNetworkImage 的1值指定系統管理安裝。</span><span class="sxs-lookup"><span data-stu-id="38f1d-123">A value of 1 for msiInstallTypeNetworkImage specifies a administrative installation.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <span data-ttu-id="38f1d-124"><dt>**msiInstallTypeDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="38f1d-124"><dt>**msiInstallTypeDefault**</dt></span></span> </dl>                     | <span data-ttu-id="38f1d-125">搜尋系統中的產品以進行修補。</span><span class="sxs-lookup"><span data-stu-id="38f1d-125">Searches system for products to patch.</span></span> <span data-ttu-id="38f1d-126">在此情況下， *InstallPackage* 必須是空字串。</span><span class="sxs-lookup"><span data-stu-id="38f1d-126">In this case, *InstallPackage* must be an empty string.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <span data-ttu-id="38f1d-127"><dt>**msiInstallSingleInstance**</dt></span><span class="sxs-lookup"><span data-stu-id="38f1d-127"><dt>**msiInstallSingleInstance**</dt></span></span> </dl>         | <span data-ttu-id="38f1d-128">修補 *InstallPackage* 所指定的產品。</span><span class="sxs-lookup"><span data-stu-id="38f1d-128">Patch the product specified by *InstallPackage*.</span></span> <span data-ttu-id="38f1d-129">*InstallPackage* 是要修補之實例的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="38f1d-129">*InstallPackage* is the product code of the instance to patch.</span></span> <span data-ttu-id="38f1d-130">這種類型的安裝需要 Windows Server 2003 或更新版本所隨附的 Windows Installer 版本，或是 Windows Installer XP SP1 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="38f1d-130">This type of installation requires the Windows Installer version shipped with Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span> <span data-ttu-id="38f1d-131">如需詳細資訊，請參閱 [安裝多個產品實例和修補程式](installing-multiple-instances-of-products-and-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="38f1d-131">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="38f1d-132">*CommandLine*</span><span class="sxs-lookup"><span data-stu-id="38f1d-132">*CommandLine*</span></span> 
</dt> <dd>

<span data-ttu-id="38f1d-133">指定要在命令列上設定的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="38f1d-133">Specifies property settings being set on the command line.</span></span> <span data-ttu-id="38f1d-134">請參閱備註一節。</span><span class="sxs-lookup"><span data-stu-id="38f1d-134">See Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f1d-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="38f1d-135">Return value</span></span>

<span data-ttu-id="38f1d-136">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="38f1d-136">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f1d-137">備註</span><span class="sxs-lookup"><span data-stu-id="38f1d-137">Remarks</span></span>

<span data-ttu-id="38f1d-138">因為轉換、來源和修補程式的清單分隔符號是分號，所以不應該將這個字元用於檔案名或路徑。</span><span class="sxs-lookup"><span data-stu-id="38f1d-138">Because the list delimiter for transforms, sources, and patches is a semicolon, this character should not be used for file names or paths.</span></span>

<span data-ttu-id="38f1d-139">套用 [小型更新](small-updates.md)或 [次要升級](minor-upgrades.md)修補程式時，需要 [**重新安裝**](reinstall.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="38f1d-139">The [**REINSTALL**](reinstall.md) property is required when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="38f1d-140">如果沒有這個屬性，就會在系統上註冊修補程式，但無法更新檔案。</span><span class="sxs-lookup"><span data-stu-id="38f1d-140">Without this property, the patch is registered on the system but cannot update files.</span></span>

<span data-ttu-id="38f1d-141">**Windows Installer 2.0：** 套用 [小型更新](small-updates.md)或 [次要升級](minor-upgrades.md)修補程式時，您必須在命令列上設定 [**重新安裝**](reinstall.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="38f1d-141">**Windows Installer 2.0:** You must set the [**REINSTALL**](reinstall.md) property on the command line when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="38f1d-142">若修補程式未使用 [自訂動作類型 51](custom-action-type-51.md)自動設定 **重新安裝** 和 [**REINSTALLMODE**](reinstallmode.md)屬性，則必須使用 *命令列* 參數明確設定 **重新安裝** 屬性。</span><span class="sxs-lookup"><span data-stu-id="38f1d-142">For patches that do not use a [Custom Action Type 51](custom-action-type-51.md) to automatically set the **REINSTALL** and [**REINSTALLMODE**](reinstallmode.md) properties, the **REINSTALL** property must be explicitly set with the *CommandLine* parameter.</span></span> <span data-ttu-id="38f1d-143">設定 [ **重新安裝** ] 屬性以列出受修補程式影響的功能，或使用 [重新安裝 = 全部] 的實際預設設定。</span><span class="sxs-lookup"><span data-stu-id="38f1d-143">Set the **REINSTALL** property to list the features affected by the patch, or use a practical default setting of "REINSTALL=ALL".</span></span> <span data-ttu-id="38f1d-144">**REINSTALLMODE** 屬性的預設值為 "omus reinstall"。</span><span class="sxs-lookup"><span data-stu-id="38f1d-144">The default value of the **REINSTALLMODE** property is "omus".</span></span>

<span data-ttu-id="38f1d-145">**Windows Installer 3.0 和更新版本：** 從 Windows Installer 版本3.0 開始，安裝 [**程式屬性是**](reinstall.md) 由安裝程式所設定，不需要在命令列上設定。</span><span class="sxs-lookup"><span data-stu-id="38f1d-145">**Windows Installer 3.0 and later:** Beginning with Windows Installer version 3.0, the [**REINSTALL**](reinstall.md) property is configured by the installer and does not need to be set on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f1d-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="38f1d-146">Requirements</span></span>



| <span data-ttu-id="38f1d-147">需求</span><span class="sxs-lookup"><span data-stu-id="38f1d-147">Requirement</span></span> | <span data-ttu-id="38f1d-148">值</span><span class="sxs-lookup"><span data-stu-id="38f1d-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f1d-149">版本</span><span class="sxs-lookup"><span data-stu-id="38f1d-149">Version</span></span><br/> | <span data-ttu-id="38f1d-150">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="38f1d-150">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="38f1d-151">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="38f1d-151">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="38f1d-152">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="38f1d-152">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="38f1d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="38f1d-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="38f1d-154"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38f1d-154"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="38f1d-155">IID</span><span class="sxs-lookup"><span data-stu-id="38f1d-155">IID</span></span><br/>     | <span data-ttu-id="38f1d-156">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="38f1d-156">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="38f1d-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38f1d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f1d-158">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="38f1d-158">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[<span data-ttu-id="38f1d-159">關於屬性</span><span class="sxs-lookup"><span data-stu-id="38f1d-159">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="38f1d-160">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="38f1d-160">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




