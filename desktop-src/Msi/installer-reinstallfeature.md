---
description: 安裝程式物件的 ReinstallFeature 方法會重新安裝功能，或更正已安裝之功能的問題。
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: ReinstallFeature 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6bac008ee7121bbcb985b9a8ff5ba02df122266
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996459"
---
# <a name="installerreinstallfeature-method"></a><span data-ttu-id="50b73-103">ReinstallFeature 方法</span><span class="sxs-lookup"><span data-stu-id="50b73-103">Installer.ReinstallFeature method</span></span>

<span data-ttu-id="50b73-104">[**安裝程式**](installer-object.md)物件的 **ReinstallFeature** 方法會重新安裝功能，或更正已安裝之功能的問題。</span><span class="sxs-lookup"><span data-stu-id="50b73-104">The **ReinstallFeature** method of the [**Installer**](installer-object.md) object reinstalls features or corrects problems with installed features.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b73-105">語法</span><span class="sxs-lookup"><span data-stu-id="50b73-105">Syntax</span></span>


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="50b73-106">參數</span><span class="sxs-lookup"><span data-stu-id="50b73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b73-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="50b73-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="50b73-108">指定產品的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="50b73-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="50b73-109">*功能*</span><span class="sxs-lookup"><span data-stu-id="50b73-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="50b73-110">指定要重新安裝的功能。</span><span class="sxs-lookup"><span data-stu-id="50b73-110">Specifies the feature to be reinstalled.</span></span> <span data-ttu-id="50b73-111">不會重新安裝指定功能的父功能或子功能。</span><span class="sxs-lookup"><span data-stu-id="50b73-111">The parent feature or child feature of the specified feature is not reinstalled.</span></span> <span data-ttu-id="50b73-112">若要重新安裝父項或子功能，您必須分別為每個或使用 [**ReinstallProduct**](installer-reinstallproduct.md)方法呼叫 **ReinstallFeature** 方法。</span><span class="sxs-lookup"><span data-stu-id="50b73-112">To reinstall the parent or child feature, you must call the **ReinstallFeature** method for each separately or use the [**ReinstallProduct**](installer-reinstallproduct.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="50b73-113">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="50b73-113">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="50b73-114">指定重新安裝的類型。</span><span class="sxs-lookup"><span data-stu-id="50b73-114">Specifies the type of reinstallation.</span></span> <span data-ttu-id="50b73-115">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="50b73-115">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="50b73-116">值</span><span class="sxs-lookup"><span data-stu-id="50b73-116">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="50b73-117">意義</span><span class="sxs-lookup"><span data-stu-id="50b73-117">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="50b73-118"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-118"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="50b73-119">只有在遺失檔案時才會重新安裝。</span><span class="sxs-lookup"><span data-stu-id="50b73-119">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="50b73-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="50b73-121">如果檔案遺失或為較舊的版本，則重新安裝。</span><span class="sxs-lookup"><span data-stu-id="50b73-121">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="50b73-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="50b73-123">如果檔案遺失或相同或較舊的版本，則重新安裝。</span><span class="sxs-lookup"><span data-stu-id="50b73-123">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="50b73-124"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-124"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="50b73-125">如果檔案遺失或不是正確的版本，則重新安裝。</span><span class="sxs-lookup"><span data-stu-id="50b73-125">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="50b73-126"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-126"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="50b73-127">檢查 sum 可執行檔，並在它們遺失或損毀時重新安裝。</span><span class="sxs-lookup"><span data-stu-id="50b73-127">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="50b73-128"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-128"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="50b73-129">無論版本為何，都會重新安裝所有檔案。</span><span class="sxs-lookup"><span data-stu-id="50b73-129">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="50b73-130"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-130"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="50b73-131">確保每 = 使用者登錄專案都需要。</span><span class="sxs-lookup"><span data-stu-id="50b73-131">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="50b73-132"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-132"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="50b73-133">確保每 = 電腦登錄專案都需要。</span><span class="sxs-lookup"><span data-stu-id="50b73-133">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="50b73-134"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-134"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="50b73-135">驗證快速鍵。</span><span class="sxs-lookup"><span data-stu-id="50b73-135">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="50b73-136"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-136"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="50b73-137">使用重新緩存來源來安裝套件。</span><span class="sxs-lookup"><span data-stu-id="50b73-137">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b73-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="50b73-138">Return value</span></span>

<span data-ttu-id="50b73-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="50b73-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b73-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="50b73-140">Requirements</span></span>



| <span data-ttu-id="50b73-141">需求</span><span class="sxs-lookup"><span data-stu-id="50b73-141">Requirement</span></span> | <span data-ttu-id="50b73-142">值</span><span class="sxs-lookup"><span data-stu-id="50b73-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b73-143">版本</span><span class="sxs-lookup"><span data-stu-id="50b73-143">Version</span></span><br/> | <span data-ttu-id="50b73-144">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="50b73-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="50b73-145">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="50b73-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="50b73-146">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="50b73-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="50b73-147">DLL</span><span class="sxs-lookup"><span data-stu-id="50b73-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="50b73-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50b73-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="50b73-149">IID</span><span class="sxs-lookup"><span data-stu-id="50b73-149">IID</span></span><br/>     | <span data-ttu-id="50b73-150">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="50b73-150">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="50b73-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50b73-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b73-152">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="50b73-152">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[<span data-ttu-id="50b73-153">安裝和設定功能</span><span class="sxs-lookup"><span data-stu-id="50b73-153">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




