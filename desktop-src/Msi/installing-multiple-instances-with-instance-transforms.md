---
description: 本主題提供安裝或重新安裝使用實例轉換之多個實例安裝的指導方針。
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: 使用實例轉換安裝多個實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026379"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a><span data-ttu-id="27c72-103">使用實例轉換安裝多個實例</span><span class="sxs-lookup"><span data-stu-id="27c72-103">Installing Multiple Instances with Instance Transforms</span></span>

<span data-ttu-id="27c72-104">本主題提供安裝或重新安裝使用實例轉換之多個實例安裝的指導方針。</span><span class="sxs-lookup"><span data-stu-id="27c72-104">This topic provides guidelines for installing or reinstalling a multiple instance installation that uses instance transforms.</span></span>

-   <span data-ttu-id="27c72-105">當您安裝具有實例轉換的新實例時，請包含 **MSINEWINSTANCE** 屬性，並設定 **MSINEWINSTANCE**= 1。</span><span class="sxs-lookup"><span data-stu-id="27c72-105">When installing a new instance with an instance transform, include the **MSINEWINSTANCE** property and set **MSINEWINSTANCE**=1.</span></span>
-   <span data-ttu-id="27c72-106">當您安裝具有實例轉換的新實例時，請包含轉換屬性，並將轉換清單中的第一個轉換設定為變更產品代碼的實例轉換。</span><span class="sxs-lookup"><span data-stu-id="27c72-106">When installing a new instance with an instance transform, include the TRANSFORMS property and set the first transform in the list of transforms to the instance transform that changes the product code.</span></span> <span data-ttu-id="27c72-107">任何自訂轉換都應遵循此清單開頭的實例轉換。</span><span class="sxs-lookup"><span data-stu-id="27c72-107">Any customization transforms should follow the instance transform at the beginning of this list.</span></span>
-   <span data-ttu-id="27c72-108">起始維護安裝和重新安裝實例的最簡單方式，就是參考實例的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="27c72-108">The easiest way to initiate a maintenance installation, and reinstall an instance, is to reference the product code of the instance.</span></span> <span data-ttu-id="27c72-109">如果您使用封裝路徑起始維護安裝，您也必須指定實例的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="27c72-109">If you initiate the maintenance installation by using the package path, you must also specify the product code of the instance.</span></span> <span data-ttu-id="27c72-110">從命令列使用/n {Product Code} 選項。</span><span class="sxs-lookup"><span data-stu-id="27c72-110">From the command line, use the /n {Product Code} option.</span></span> <span data-ttu-id="27c72-111">從程式碼或腳本中，使用 **MSIINSTANCEGUID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="27c72-111">From code or script, use the **MSIINSTANCEGUID** property.</span></span>

<span data-ttu-id="27c72-112">下列範例示範如何從命令列安裝新的實例，其中實例轉換的前面會加上冒號，以指定轉換內嵌于封裝中。</span><span class="sxs-lookup"><span data-stu-id="27c72-112">The following example shows installing a new instance from a command line where the instance transform is prefixed by a colon which specifies that the transform is embedded in the package.</span></span>

<span data-ttu-id="27c72-113">**msiexec/I mypackage.msi 轉換 =： instance。 mst MSINEWINSTANCE = 1/qb**</span><span class="sxs-lookup"><span data-stu-id="27c72-113">**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**</span></span>

<span data-ttu-id="27c72-114">下列範例示範如何使用 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)安裝新的實例。</span><span class="sxs-lookup"><span data-stu-id="27c72-114">The following example shows installing a new instance using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

<span data-ttu-id="27c72-115">下列範例示範如何從腳本安裝新的實例。</span><span class="sxs-lookup"><span data-stu-id="27c72-115">The following example shows installing the new instance from script.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

<span data-ttu-id="27c72-116">下列範例會重新安裝實例，而不需要重新快取套件。</span><span class="sxs-lookup"><span data-stu-id="27c72-116">The following example reinstalls an instance without re-caching the package.</span></span> <span data-ttu-id="27c72-117">實例是由其產品代碼所參考 {00000001-0002-0000-0000-624474736554} 。</span><span class="sxs-lookup"><span data-stu-id="27c72-117">The instance is referred to by its product code {00000001-0002-0000-0000-624474736554}.</span></span>

<span data-ttu-id="27c72-118">**msiexec/I {00000001-0002-0000-0000-624474736554} 重新安裝 = ALL REINSTALLMODE = omus reinstall/qb**</span><span class="sxs-lookup"><span data-stu-id="27c72-118">**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**</span></span>

<span data-ttu-id="27c72-119">下列範例會重新安裝實例，並從命令列重新快取套件。</span><span class="sxs-lookup"><span data-stu-id="27c72-119">The following example reinstalls an instance and re-caches the package from the command line.</span></span> <span data-ttu-id="27c72-120">封裝路徑會參考此實例。</span><span class="sxs-lookup"><span data-stu-id="27c72-120">The instance is referred to by the package path.</span></span> <span data-ttu-id="27c72-121">如果產品原本是隨著實例轉換而安裝，您只需要包含/n {Product Code} 選項。</span><span class="sxs-lookup"><span data-stu-id="27c72-121">You are only required to include the /n {Product Code} option if the product is originally installed with an instance transform.</span></span>

<span data-ttu-id="27c72-122">**msiexec/I c： \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} 重新安裝 = ALL REINSTALLMODE = vomus reinstall/qb**</span><span class="sxs-lookup"><span data-stu-id="27c72-122">**msiexec /I c:\\newpath\\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**</span></span>

<span data-ttu-id="27c72-123">下列範例會使用 **MsiInstallProduct** 來重新安裝實例，並快取封裝。</span><span class="sxs-lookup"><span data-stu-id="27c72-123">The following example reinstalls an instance and caches the package using **MsiInstallProduct**.</span></span> <span data-ttu-id="27c72-124">封裝路徑會參考此實例。</span><span class="sxs-lookup"><span data-stu-id="27c72-124">The instance is referred to by the package path.</span></span> <span data-ttu-id="27c72-125">您可以使用 **MSIINSTANCEGUID** 屬性來提供實例的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="27c72-125">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

<span data-ttu-id="27c72-126">下列範例會重新安裝實例，並使用腳本來快取封裝。</span><span class="sxs-lookup"><span data-stu-id="27c72-126">The following example reinstalls an instance and caches the package using script.</span></span> <span data-ttu-id="27c72-127">您可以使用 **MSIINSTANCEGUID** 屬性來提供實例的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="27c72-127">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

<span data-ttu-id="27c72-128">下列範例示範如何使用命令列通告實例。</span><span class="sxs-lookup"><span data-stu-id="27c72-128">The following example shows how to advertise an instance using the command line.</span></span>

<span data-ttu-id="27c72-129">**msiexec/jm mypackage.msi/t： instance. mst/c/qb**</span><span class="sxs-lookup"><span data-stu-id="27c72-129">**msiexec /jm mypackage.msi /t :instance.mst /c /qb**</span></span>

<span data-ttu-id="27c72-130">下列範例示範如何使用 **MsiAdvertiseProductEx** 來安裝以公告實例。</span><span class="sxs-lookup"><span data-stu-id="27c72-130">The following example shows how to install to advertise an instance using **MsiAdvertiseProductEx**.</span></span>

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

<span data-ttu-id="27c72-131">下列範例顯示如何從命令列將修補程式套用至實例。</span><span class="sxs-lookup"><span data-stu-id="27c72-131">The following example shows how to apply a patch to an instance from a command line.</span></span> <span data-ttu-id="27c72-132">如果產品原本是隨著實例轉換而安裝，您只需要包含/n {Product Code} 選項。</span><span class="sxs-lookup"><span data-stu-id="27c72-132">You are only required to include the /n {Product Code} option if the product was originally installed with an instance transform.</span></span>

<span data-ttu-id="27c72-133">**msiexec/p mypatch .msp/n {00000001-0002-0000-0000-624474736554} /qb**</span><span class="sxs-lookup"><span data-stu-id="27c72-133">**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**</span></span>

<span data-ttu-id="27c72-134">下列範例示範如何使用 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)將修補程式套用至實例安裝。</span><span class="sxs-lookup"><span data-stu-id="27c72-134">The following example shows how to apply a patch to an instance installation using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span></span>

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

<span data-ttu-id="27c72-135">如需詳細資訊，請參閱 [安裝多個產品的實例和修補程式](installing-multiple-instances-of-products-and-patches.md) ，並 [使用實例轉換來撰寫多個實例](authoring-multiple-instances-with-instance-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="27c72-135">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) and [Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md).</span></span>

 

 



