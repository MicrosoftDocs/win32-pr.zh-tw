---
description: 安裝程式物件的 ProvideQualifiedComponent 方法會傳回完整的元件路徑，並執行任何必要的安裝。 如有必要，這個方法會提示輸入來源並遞增功能的使用計數。
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: ProvideQualifiedComponent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977560"
---
# <a name="installerprovidequalifiedcomponent-method"></a><span data-ttu-id="eed93-104">ProvideQualifiedComponent 方法</span><span class="sxs-lookup"><span data-stu-id="eed93-104">Installer.ProvideQualifiedComponent method</span></span>

<span data-ttu-id="eed93-105">[**安裝程式**](installer-object.md)物件的 **ProvideQualifiedComponent** 方法會傳回完整的元件路徑，並執行任何必要的安裝。</span><span class="sxs-lookup"><span data-stu-id="eed93-105">The **ProvideQualifiedComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="eed93-106">如有必要，這個方法會提示輸入來源並遞增功能的使用計數。</span><span class="sxs-lookup"><span data-stu-id="eed93-106">If necessary, this method prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed93-107">語法</span><span class="sxs-lookup"><span data-stu-id="eed93-107">Syntax</span></span>


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="eed93-108">參數</span><span class="sxs-lookup"><span data-stu-id="eed93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed93-109">*類別*</span><span class="sxs-lookup"><span data-stu-id="eed93-109">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="eed93-110">指定所要求元件的元件識別碼。</span><span class="sxs-lookup"><span data-stu-id="eed93-110">Specifies the component ID for the requested component.</span></span> <span data-ttu-id="eed93-111">這可能不是元件本身的 GUID，而是提供正確功能的伺服器，如同 [PublishComponent 資料表](publishcomponent-table.md)的 [元件] 資料行。</span><span class="sxs-lookup"><span data-stu-id="eed93-111">This may not be the GUID for the component itself but rather a server that provides the correct functionality, as in the ComponentId column of the [PublishComponent table](publishcomponent-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="eed93-112">*Qualifier*</span><span class="sxs-lookup"><span data-stu-id="eed93-112">*Qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="eed93-113">從 [PublishComponent 資料表](publishcomponent-table.md)) 指定 (的廣告元件清單中的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="eed93-113">Specifies a qualifier into a list of advertising components (from [PublishComponent table](publishcomponent-table.md)).</span></span>

</dd> <dt>

<span data-ttu-id="eed93-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="eed93-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="eed93-115">定義安裝模式。</span><span class="sxs-lookup"><span data-stu-id="eed93-115">Defines the installation mode.</span></span> <span data-ttu-id="eed93-116">此參數可以是下表所示的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="eed93-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="eed93-117">InstallMode</span><span class="sxs-lookup"><span data-stu-id="eed93-117">InstallMode</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="eed93-118">意義</span><span class="sxs-lookup"><span data-stu-id="eed93-118">Meaning</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="eed93-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eed93-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                 | <span data-ttu-id="eed93-120">提供元件，並執行任何必要的安裝。</span><span class="sxs-lookup"><span data-stu-id="eed93-120">Provides the component, performing any necessary installation.</span></span><br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="eed93-121"><dt>**msiInstallModeExisting**</dt> <dt>– 1</dt></span><span class="sxs-lookup"><span data-stu-id="eed93-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                            | <span data-ttu-id="eed93-122">只有在功能存在時才會提供元件;否則會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="eed93-122">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="eed93-123">這個模式會確認元件的金鑰檔是否存在。</span><span class="sxs-lookup"><span data-stu-id="eed93-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="eed93-124"><dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="eed93-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                                | <span data-ttu-id="eed93-125">只有在功能存在時才會提供元件;否則會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="eed93-125">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="eed93-126">此模式只會檢查元件是否已註冊，但不會驗證元件的金鑰檔是否存在。</span><span class="sxs-lookup"><span data-stu-id="eed93-126">This mode only checks that the component is registered but does not verify the existence of the component's key file.</span></span><br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="eed93-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="eed93-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                    | <span data-ttu-id="eed93-128">只有在具有 *MsiInstallStateLocal* InstallState 參數的功能存在時，才會提供元件路徑。</span><span class="sxs-lookup"><span data-stu-id="eed93-128">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="eed93-129">這會檢查元件的註冊，但不會驗證元件的金鑰檔是否存在。</span><span class="sxs-lookup"><span data-stu-id="eed93-129">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="eed93-130"><dt>**msiReinstallMode 旗標**</dt> <dt></dt>的組合</span><span class="sxs-lookup"><span data-stu-id="eed93-130"><dt>**combination of the msiReinstallMode flags**</dt> <dt> </dt></span></span> </dl> | <span data-ttu-id="eed93-131">使用 *ReinstallMode* 參數的這個參數，呼叫 [**ReinstallFeature**](installer-reinstallfeature.md)來重新安裝此功能，然後提供元件。</span><span class="sxs-lookup"><span data-stu-id="eed93-131">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed93-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="eed93-132">Return value</span></span>

<span data-ttu-id="eed93-133">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="eed93-133">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed93-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="eed93-134">Requirements</span></span>



| <span data-ttu-id="eed93-135">需求</span><span class="sxs-lookup"><span data-stu-id="eed93-135">Requirement</span></span> | <span data-ttu-id="eed93-136">值</span><span class="sxs-lookup"><span data-stu-id="eed93-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed93-137">版本</span><span class="sxs-lookup"><span data-stu-id="eed93-137">Version</span></span><br/> | <span data-ttu-id="eed93-138">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="eed93-138">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eed93-139">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="eed93-139">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eed93-140">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="eed93-140">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="eed93-141">DLL</span><span class="sxs-lookup"><span data-stu-id="eed93-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="eed93-142"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eed93-142"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="eed93-143">IID</span><span class="sxs-lookup"><span data-stu-id="eed93-143">IID</span></span><br/>     | <span data-ttu-id="eed93-144">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eed93-144">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="eed93-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eed93-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed93-146">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="eed93-146">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




