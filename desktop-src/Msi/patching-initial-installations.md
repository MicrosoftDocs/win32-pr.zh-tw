---
description: 當您第一次使用 PATCH 屬性安裝應用程式時，可以套用 Windows Installer Patch (MSP) 。
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: 修補初始安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945325"
---
# <a name="patching-initial-installations"></a><span data-ttu-id="e2f0e-103">修補初始安裝</span><span class="sxs-lookup"><span data-stu-id="e2f0e-103">Patching Initial Installations</span></span>

<span data-ttu-id="e2f0e-104">當您第一次使用 [**patch**](patch.md) 屬性安裝應用程式時，可以套用 Windows Installer PATCH (MSP) 。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-104">A Windows Installer Patch (MSP) can be applied when installing an application for the first time by using the [**PATCH**](patch.md) property.</span></span>

<span data-ttu-id="e2f0e-105">若要在第一次安裝應用程式時套用修補程式，則必須在命令列上設定 [**patch**](patch.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-105">To apply a patch the first time the application is installed, the [**PATCH**](patch.md) property must be set on the command line.</span></span> <span data-ttu-id="e2f0e-106">在命令列上，將修補程式的完整路徑指定為 "PATCH = {*patch to patch*}" 屬性-值配對。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-106">Specify the full path to the patch on the command line as the "PATCH={*path to patch*}" property-value pair.</span></span>

<span data-ttu-id="e2f0e-107">請注意，在命令列上指定 [**patch**](patch.md) 屬性會覆寫使用 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) 或/p [命令列選項](command-line-options.md)時所執行的修補程式適用性檢查。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-107">Note that specifying the [**PATCH**](patch.md) property on the command line overrides the patch applicability checks performed when using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md).</span></span>

<span data-ttu-id="e2f0e-108">如果使用 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) 或/P [命令列選項](command-line-options.md)來套用修補程式，安裝程式會將目前安裝在電腦上的應用程式，與符合在 [**範本摘要**](template-summary.md) 屬性中接收修補程式的產品代碼清單進行比較。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-108">If a patch is applied using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md), the installer compares the applications currently installed on the computer to the list of product codes eligible to receive the patch in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="e2f0e-109">當您在命令列上設定 [**PATCH**](patch.md) 屬性以在第一次安裝時安裝時，有資格接收修補程式的應用程式是由修補程式套件中內嵌之轉換的驗證條件所決定。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-109">When you set the [**PATCH**](patch.md) property on the command line to install on first installation, the applications eligible to receive the patch is determined by validation conditions on the transforms embedded in the patch package.</span></span> <span data-ttu-id="e2f0e-110">產生修補程式套件的建議方法是使用修補程式建立工具，例如 [Msimsp.exe](msimsp-exe.md) 和 [PATCHWIZ.DLL](patchwiz-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-110">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and [PATCHWIZ.DLL](patchwiz-dll.md).</span></span> <span data-ttu-id="e2f0e-111">修補程式中轉換的驗證條件源自于 Patch 建立屬性 (. pcp) 檔案的 [TargetImages](targetimages-table-patchwiz-dll-.md) 資料表中的 ProductValidateFlags 資料行。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-111">The validation conditions on transforms in the patch originate from the ProductValidateFlags column in the [TargetImages](targetimages-table-patchwiz-dll-.md) table of the Patch Creation Properties (.pcp) file.</span></span>

<span data-ttu-id="e2f0e-112">第一次使用命令列、另一個應用程式或腳本安裝應用程式時，可以套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-112">The patch can be applied the first time the application is installed by a command line, another application, or script.</span></span>

<span data-ttu-id="e2f0e-113">以下顯示從命令列進行的第一次修補。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-113">The following shows first-time patching from the command line.</span></span>

<span data-ttu-id="e2f0e-114">**msiexec/i** *package.msi* **PATCH =**_"c： \\ directory \\ PATCH .msp"_</span><span class="sxs-lookup"><span data-stu-id="e2f0e-114">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp"_</span></span>

<span data-ttu-id="e2f0e-115">以下顯示來自另一個應用程式的第一次修補。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-115">The following shows first-time patching from another application.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

<span data-ttu-id="e2f0e-116">以下顯示腳本的第一次修補。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-116">The following shows first-time patching from script.</span></span>


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



<span data-ttu-id="e2f0e-117">\* \* Windows Installer 3.0 和更新版本： \* \*</span><span class="sxs-lookup"><span data-stu-id="e2f0e-117">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="e2f0e-118">從 Windows Installer 版本3.0 開始，在第一次安裝應用程式時，可以套用多個修補程式。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-118">Beginning with Windows Installer version 3.0, multiple patches can be applied when installing an application for the first time.</span></span> <span data-ttu-id="e2f0e-119">將 [**PATCH**](patch.md) 屬性設定為以分號分隔的修補程式完整路徑清單。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-119">Set the [**PATCH**](patch.md) property to a semicolon delimited list of the patches' full paths.</span></span> <span data-ttu-id="e2f0e-120">以下顯示從命令列的多個修補程式的第一次修補。</span><span class="sxs-lookup"><span data-stu-id="e2f0e-120">The following shows first-time patching of multiple patches from the command line.</span></span>

<span data-ttu-id="e2f0e-121">**msiexec/i** *package.msi* **PATCH =**_"c： \\ directory \\ PATCH .msp; c： \\ directory \\ patch2 .msp; c： \\ directory \\ patch3 .msp"_</span><span class="sxs-lookup"><span data-stu-id="e2f0e-121">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp;c:\\directory\\patch2.msp;c:\\directory\\patch3.msp"_</span></span>

 

 



