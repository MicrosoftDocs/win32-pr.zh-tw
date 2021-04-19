---
description: 安裝程式物件的 ProvideComponent 方法會傳回完整的元件路徑，並執行任何必要的安裝。
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: ProvideComponent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985570"
---
# <a name="installerprovidecomponent-method"></a><span data-ttu-id="e777f-103">ProvideComponent 方法</span><span class="sxs-lookup"><span data-stu-id="e777f-103">Installer.ProvideComponent method</span></span>

<span data-ttu-id="e777f-104">[**安裝程式**](installer-object.md)物件的 **ProvideComponent** 方法會傳回完整的元件路徑，並執行任何必要的安裝。</span><span class="sxs-lookup"><span data-stu-id="e777f-104">The **ProvideComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="e777f-105">如有必要，[**安裝程式**](installer-object.md)物件的 **ProvideComponent** 方法會提示輸入來源並遞增功能的使用計數。</span><span class="sxs-lookup"><span data-stu-id="e777f-105">If necessary, the **ProvideComponent** method of the [**Installer**](installer-object.md) object prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="e777f-106">語法</span><span class="sxs-lookup"><span data-stu-id="e777f-106">Syntax</span></span>


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="e777f-107">參數</span><span class="sxs-lookup"><span data-stu-id="e777f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e777f-108">*產品*</span><span class="sxs-lookup"><span data-stu-id="e777f-108">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="e777f-109">指定產品的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="e777f-109">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="e777f-110">*功能*</span><span class="sxs-lookup"><span data-stu-id="e777f-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="e777f-111">指定包含元件之功能的功能識別碼。</span><span class="sxs-lookup"><span data-stu-id="e777f-111">Specifies the feature ID of the feature containing the component.</span></span>

</dd> <dt>

<span data-ttu-id="e777f-112">*元件*</span><span class="sxs-lookup"><span data-stu-id="e777f-112">*Component*</span></span> 
</dt> <dd>

<span data-ttu-id="e777f-113">指定元件代碼。</span><span class="sxs-lookup"><span data-stu-id="e777f-113">Specifies the component code.</span></span>

</dd> <dt>

<span data-ttu-id="e777f-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="e777f-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="e777f-115">定義安裝模式。</span><span class="sxs-lookup"><span data-stu-id="e777f-115">Defines the installation mode.</span></span> <span data-ttu-id="e777f-116">此參數可以是下表所示的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e777f-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="e777f-117">Name</span><span class="sxs-lookup"><span data-stu-id="e777f-117">Name</span></span>                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="e777f-118">意義</span><span class="sxs-lookup"><span data-stu-id="e777f-118">Meaning</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="e777f-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e777f-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                | <span data-ttu-id="e777f-120">提供元件路徑，視需要執行任何安裝。</span><span class="sxs-lookup"><span data-stu-id="e777f-120">Provides the component path, performing any installation, if necessary.</span></span><br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="e777f-121"><dt>**msiInstallModeExisting**</dt> <dt>– 1</dt></span><span class="sxs-lookup"><span data-stu-id="e777f-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                           | <span data-ttu-id="e777f-122">只有在功能存在時，才會提供元件路徑;否則，會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="e777f-122">Provides the component path only if the feature exists; otherwise, returns an empty string.</span></span> <span data-ttu-id="e777f-123">這個模式會確認元件的金鑰檔是否存在。</span><span class="sxs-lookup"><span data-stu-id="e777f-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="e777f-124"><dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="e777f-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                               | <span data-ttu-id="e777f-125">只有在功能存在時，才會提供元件路徑。</span><span class="sxs-lookup"><span data-stu-id="e777f-125">Provides the component path only if the feature exists.</span></span> <span data-ttu-id="e777f-126">否則，會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="e777f-126">Otherwise, returns an empty string.</span></span> <span data-ttu-id="e777f-127">此模式會檢查元件的註冊，但不會驗證元件的金鑰檔是否存在。</span><span class="sxs-lookup"><span data-stu-id="e777f-127">This mode checks the component's registration but does not verify the existence of the component's key file.</span></span><br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="e777f-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="e777f-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                   | <span data-ttu-id="e777f-129">只有在具有 *MsiInstallStateLocal* InstallState 參數的功能存在時，才會提供元件路徑。</span><span class="sxs-lookup"><span data-stu-id="e777f-129">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="e777f-130">這會檢查元件的註冊，但不會驗證元件的金鑰檔是否存在。</span><span class="sxs-lookup"><span data-stu-id="e777f-130">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="e777f-131"><dt>**msiReinstallMode 旗標的組合**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="e777f-131"><dt>**combination of the msiReinstallMode flags**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="e777f-132">使用 *ReinstallMode* 參數的這個參數，呼叫 [**ReinstallFeature**](installer-reinstallfeature.md)來重新安裝此功能，然後提供元件。</span><span class="sxs-lookup"><span data-stu-id="e777f-132">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e777f-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="e777f-133">Return value</span></span>

<span data-ttu-id="e777f-134">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e777f-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e777f-135">備註</span><span class="sxs-lookup"><span data-stu-id="e777f-135">Remarks</span></span>

<span data-ttu-id="e777f-136">**ProvideComponent** 方法會結合 [**UseFeature**](installer-usefeature.md)、 [**ConfigureFeature**](installer-configurefeature.md)和 [**ComponentPath**](installer-componentpath.md)的功能。</span><span class="sxs-lookup"><span data-stu-id="e777f-136">The **ProvideComponent** method combines the functionality of [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md), and [**ComponentPath**](installer-componentpath.md).</span></span> <span data-ttu-id="e777f-137">**ProvideComponent** 方法會簡化呼叫序列，但也會增加使用計數，且應該謹慎使用，以避免使用次數不正確。</span><span class="sxs-lookup"><span data-stu-id="e777f-137">The **ProvideComponent** method simplifies the calling sequence, but it also increments the usage count and should be used with caution to prevent inaccurate usage counts.</span></span> <span data-ttu-id="e777f-138">**ProvideComponent** 方法也提供比一系列個別呼叫先前所述的方法和屬性更少的彈性。</span><span class="sxs-lookup"><span data-stu-id="e777f-138">The **ProvideComponent** method also provides less flexibility than a series of individual calls to the methods and properties previously mentioned.</span></span>

<span data-ttu-id="e777f-139">如果應用程式正在從非預期的情況下復原，則應用程式可能已被呼叫 [**UseFeature**](installer-usefeature.md) 並增加了使用計數。</span><span class="sxs-lookup"><span data-stu-id="e777f-139">If the application is recovering from an unexpected situation, the application has probably already called [**UseFeature**](installer-usefeature.md) and incremented the usage count.</span></span> <span data-ttu-id="e777f-140">在此情況下，應用程式應呼叫 [**ConfigureFeature**](installer-configurefeature.md) 方法，而不是 **ProvideComponent** 方法，以避免遞增使用計數。</span><span class="sxs-lookup"><span data-stu-id="e777f-140">In this case, the application should avoid incrementing the usage count by calling the [**ConfigureFeature**](installer-configurefeature.md) method instead of the **ProvideComponent** method.</span></span>

<span data-ttu-id="e777f-141">MsiInstallModeExisting 選項不能搭配 msiReinstallMode 旗標一起使用。</span><span class="sxs-lookup"><span data-stu-id="e777f-141">The msiInstallModeExisting option cannot be used in combination with msiReinstallMode flags.</span></span>

## <a name="requirements"></a><span data-ttu-id="e777f-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="e777f-142">Requirements</span></span>



| <span data-ttu-id="e777f-143">需求</span><span class="sxs-lookup"><span data-stu-id="e777f-143">Requirement</span></span> | <span data-ttu-id="e777f-144">值</span><span class="sxs-lookup"><span data-stu-id="e777f-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e777f-145">版本</span><span class="sxs-lookup"><span data-stu-id="e777f-145">Version</span></span><br/> | <span data-ttu-id="e777f-146">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e777f-146">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e777f-147">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e777f-147">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e777f-148">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e777f-148">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e777f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e777f-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="e777f-150"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e777f-150"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e777f-151">IID</span><span class="sxs-lookup"><span data-stu-id="e777f-151">IID</span></span><br/>     | <span data-ttu-id="e777f-152">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e777f-152">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e777f-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e777f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e777f-154">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="e777f-154">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




