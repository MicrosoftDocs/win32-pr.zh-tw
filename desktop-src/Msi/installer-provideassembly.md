---
description: 安裝程式物件的 ProvideAssembly 方法會傳回元件的已安裝路徑。
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: 安裝程式：:P rovideAssembly 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994852"
---
# <a name="installerprovideassembly-method"></a><span data-ttu-id="3c580-103">安裝程式：:P rovideAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="3c580-103">Installer::ProvideAssembly method</span></span>

<span data-ttu-id="3c580-104">[**安裝程式**](installer-object.md)物件的 **ProvideAssembly** 方法會傳回元件的已安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="3c580-104">The **ProvideAssembly** method of the [**Installer**](installer-object.md) object returns the installed path of an assembly.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c580-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c580-105">Syntax</span></span>


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a><span data-ttu-id="3c580-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c580-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c580-107">*裝配*</span><span class="sxs-lookup"><span data-stu-id="3c580-107">*assembly*</span></span> 
</dt> <dd>

<span data-ttu-id="3c580-108">要查詢之已安裝元件的強式名稱。</span><span class="sxs-lookup"><span data-stu-id="3c580-108">The strong name of installed assembly that is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="3c580-109">*appCoNtext*</span><span class="sxs-lookup"><span data-stu-id="3c580-109">*appContext*</span></span> 
</dt> <dd>

<span data-ttu-id="3c580-110">全域程式集的設為 null。</span><span class="sxs-lookup"><span data-stu-id="3c580-110">Set to null for global assemblies.</span></span> <span data-ttu-id="3c580-111">若為私用元件，請將 *appCoNtext* 設定為應用程式佈建檔的完整路徑，或設定為私用元件之應用程式的可執行檔完整路徑。</span><span class="sxs-lookup"><span data-stu-id="3c580-111">For private assemblies, set *appContext* to the full path of the application configuration file or to the full path of the executable file of the application to which the assembly has been made private.</span></span>

</dd> <dt>

<span data-ttu-id="3c580-112">*installMode*</span><span class="sxs-lookup"><span data-stu-id="3c580-112">*installMode*</span></span> 
</dt> <dd>

<span data-ttu-id="3c580-113">定義安裝模式。</span><span class="sxs-lookup"><span data-stu-id="3c580-113">Defines the installation mode.</span></span> <span data-ttu-id="3c580-114">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3c580-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3c580-115">值</span><span class="sxs-lookup"><span data-stu-id="3c580-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="3c580-116">意義</span><span class="sxs-lookup"><span data-stu-id="3c580-116">Meaning</span></span>                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="3c580-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c580-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                                | <span data-ttu-id="3c580-118">提供元件，並執行提供元件所需的任何安裝。</span><span class="sxs-lookup"><span data-stu-id="3c580-118">Provide the component and perform any installation necessary to provide the component.</span></span> <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="3c580-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="3c580-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span></span> </dl>                                                                                           | <span data-ttu-id="3c580-120">只有在功能存在時，才提供元件。</span><span class="sxs-lookup"><span data-stu-id="3c580-120">Provide the component only if the feature exists.</span></span> <span data-ttu-id="3c580-121">此選項會確認元件是否存在。</span><span class="sxs-lookup"><span data-stu-id="3c580-121">This option will verify that the assembly exists.</span></span><br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="3c580-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="3c580-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span></span> </dl>                                                                               | <span data-ttu-id="3c580-123">只有在功能存在時，才提供元件。</span><span class="sxs-lookup"><span data-stu-id="3c580-123">Provide the component only if the feature exists.</span></span> <span data-ttu-id="3c580-124">此選項不會驗證元件是否存在。</span><span class="sxs-lookup"><span data-stu-id="3c580-124">This option does not verify that the assembly exists.</span></span><br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="3c580-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="3c580-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span></span> </dl>                                                   | <span data-ttu-id="3c580-126">只有在元件安裝在本機時，才會提供元件。</span><span class="sxs-lookup"><span data-stu-id="3c580-126">Provides the assembly only if the assembly is installed local.</span></span><br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <span data-ttu-id="3c580-127"><dt>**ReinstallFeature 所使用之旗標的組合 [](installer-reinstallfeature.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="3c580-127"><dt>**Combination of the flags used by [**ReinstallFeature**](installer-reinstallfeature.md)**</dt></span></span> </dl> | <span data-ttu-id="3c580-128">呼叫 [**ReinstallFeature**](installer-reinstallfeature.md) 方法，以使用這個 *ReinstallMode* 參數重新安裝此功能，然後傳回元件路徑。</span><span class="sxs-lookup"><span data-stu-id="3c580-128">Calls the [**ReinstallFeature**](installer-reinstallfeature.md) method to reinstall the feature using this parameter for *ReinstallMode*, and then returns the assembly path.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3c580-129">*assemblyInfo*</span><span class="sxs-lookup"><span data-stu-id="3c580-129">*assemblyInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3c580-130">元件資訊和元件類型。</span><span class="sxs-lookup"><span data-stu-id="3c580-130">Assembly information and assembly type.</span></span> <span data-ttu-id="3c580-131">設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3c580-131">Set to one of the following values.</span></span>



| <span data-ttu-id="3c580-132">值</span><span class="sxs-lookup"><span data-stu-id="3c580-132">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="3c580-133">意義</span><span class="sxs-lookup"><span data-stu-id="3c580-133">Meaning</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <span data-ttu-id="3c580-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c580-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="3c580-135">.NET 元件。</span><span class="sxs-lookup"><span data-stu-id="3c580-135">A .NET assembly.</span></span><br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <span data-ttu-id="3c580-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c580-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="3c580-137">Win32 並存元件。</span><span class="sxs-lookup"><span data-stu-id="3c580-137">A Win32 side-by-side assembly.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c580-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c580-138">Return value</span></span>

<span data-ttu-id="3c580-139">已安裝元件的路徑。</span><span class="sxs-lookup"><span data-stu-id="3c580-139">The path to the installed assembly.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c580-140">備註</span><span class="sxs-lookup"><span data-stu-id="3c580-140">Remarks</span></span>

<span data-ttu-id="3c580-141">**ProvideAssembly** 方法會使用 [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)函數。</span><span class="sxs-lookup"><span data-stu-id="3c580-141">The **ProvideAssembly** method uses the [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) function.</span></span>

## <a name="examples"></a><span data-ttu-id="3c580-142">範例</span><span class="sxs-lookup"><span data-stu-id="3c580-142">Examples</span></span>

<span data-ttu-id="3c580-143">下列範例腳本示範如何使用 ProvideAssembly 方法。</span><span class="sxs-lookup"><span data-stu-id="3c580-143">The following sample script demonstrates the use of the ProvideAssembly method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a><span data-ttu-id="3c580-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c580-144">Requirements</span></span>



| <span data-ttu-id="3c580-145">需求</span><span class="sxs-lookup"><span data-stu-id="3c580-145">Requirement</span></span> | <span data-ttu-id="3c580-146">值</span><span class="sxs-lookup"><span data-stu-id="3c580-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c580-147">版本</span><span class="sxs-lookup"><span data-stu-id="3c580-147">Version</span></span><br/> | <span data-ttu-id="3c580-148">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="3c580-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3c580-149">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="3c580-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3c580-150">Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5</span><span class="sxs-lookup"><span data-stu-id="3c580-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="3c580-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3c580-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c580-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c580-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="3c580-153">IID</span><span class="sxs-lookup"><span data-stu-id="3c580-153">IID</span></span><br/>     | <span data-ttu-id="3c580-154">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3c580-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="3c580-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c580-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c580-156">**安裝程式**</span><span class="sxs-lookup"><span data-stu-id="3c580-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="3c580-157">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="3c580-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




