---
description: 安裝程式物件的 ReinstallProduct 方法會重新安裝產品，或更正已安裝產品中的安裝問題。
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: ReinstallProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1570f5a0dc607b4a011a5b4276a243c59a64392d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976116"
---
# <a name="installerreinstallproduct-method"></a><span data-ttu-id="21290-103">ReinstallProduct 方法</span><span class="sxs-lookup"><span data-stu-id="21290-103">Installer.ReinstallProduct method</span></span>

<span data-ttu-id="21290-104">[**安裝程式**](installer-object.md)物件的 **ReinstallProduct** 方法會重新安裝產品，或更正已安裝產品中的安裝問題。</span><span class="sxs-lookup"><span data-stu-id="21290-104">The **ReinstallProduct** method of the [**Installer**](installer-object.md) object reinstalls a product or corrects installation problems in an installed product.</span></span>

## <a name="syntax"></a><span data-ttu-id="21290-105">語法</span><span class="sxs-lookup"><span data-stu-id="21290-105">Syntax</span></span>


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="21290-106">參數</span><span class="sxs-lookup"><span data-stu-id="21290-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21290-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="21290-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="21290-108">指定產品的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="21290-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="21290-109">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="21290-109">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="21290-110">指定重新安裝的類型。</span><span class="sxs-lookup"><span data-stu-id="21290-110">Specifies the type of reinstallation.</span></span> <span data-ttu-id="21290-111">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="21290-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="21290-112">值</span><span class="sxs-lookup"><span data-stu-id="21290-112">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="21290-113">意義</span><span class="sxs-lookup"><span data-stu-id="21290-113">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="21290-114"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-114"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="21290-115">只有在遺失檔案時才會重新安裝。</span><span class="sxs-lookup"><span data-stu-id="21290-115">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="21290-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="21290-117">如果檔案遺失或為較舊的版本，則重新安裝。</span><span class="sxs-lookup"><span data-stu-id="21290-117">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="21290-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="21290-119">如果檔案遺失或相同或較舊的版本，則重新安裝。</span><span class="sxs-lookup"><span data-stu-id="21290-119">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="21290-120"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-120"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="21290-121">如果檔案遺失或不是正確的版本，則重新安裝。</span><span class="sxs-lookup"><span data-stu-id="21290-121">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="21290-122"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-122"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="21290-123">檢查 sum 可執行檔，並在它們遺失或損毀時重新安裝。</span><span class="sxs-lookup"><span data-stu-id="21290-123">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="21290-124"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-124"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="21290-125">無論版本為何，都會重新安裝所有檔案。</span><span class="sxs-lookup"><span data-stu-id="21290-125">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="21290-126"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-126"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="21290-127">確保每 = 使用者登錄專案都需要。</span><span class="sxs-lookup"><span data-stu-id="21290-127">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="21290-128"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-128"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="21290-129">確保每 = 電腦登錄專案都需要。</span><span class="sxs-lookup"><span data-stu-id="21290-129">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="21290-130"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-130"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="21290-131">驗證快速鍵。</span><span class="sxs-lookup"><span data-stu-id="21290-131">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="21290-132"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="21290-132"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="21290-133">使用重新緩存來源來安裝套件。</span><span class="sxs-lookup"><span data-stu-id="21290-133">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21290-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="21290-134">Return value</span></span>

<span data-ttu-id="21290-135">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="21290-135">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21290-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="21290-136">Requirements</span></span>



| <span data-ttu-id="21290-137">需求</span><span class="sxs-lookup"><span data-stu-id="21290-137">Requirement</span></span> | <span data-ttu-id="21290-138">值</span><span class="sxs-lookup"><span data-stu-id="21290-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21290-139">版本</span><span class="sxs-lookup"><span data-stu-id="21290-139">Version</span></span><br/> | <span data-ttu-id="21290-140">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="21290-140">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="21290-141">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="21290-141">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="21290-142">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="21290-142">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="21290-143">DLL</span><span class="sxs-lookup"><span data-stu-id="21290-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="21290-144"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21290-144"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="21290-145">IID</span><span class="sxs-lookup"><span data-stu-id="21290-145">IID</span></span><br/>     | <span data-ttu-id="21290-146">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="21290-146">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="21290-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21290-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21290-148">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="21290-148">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[<span data-ttu-id="21290-149">安裝和設定功能</span><span class="sxs-lookup"><span data-stu-id="21290-149">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




