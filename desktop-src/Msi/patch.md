---
description: 安裝程式會藉由呼叫 MsiApplyPatch、MsiApplyMultiplePatches 或/p 命令列選項，將 PATCH 屬性設為要套用的修補程式清單。
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: PATCH 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983142"
---
# <a name="patch-property"></a><span data-ttu-id="623ad-103">PATCH 屬性</span><span class="sxs-lookup"><span data-stu-id="623ad-103">PATCH property</span></span>

<span data-ttu-id="623ad-104">安裝程式會藉由呼叫 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)、 [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)或/p [命令列選項](command-line-options.md)，將 **PATCH** 屬性設為要套用的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="623ad-104">The installer sets the **PATCH** property to a list of patches being applied by calling [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) or the /p [Command Line Option](command-line-options.md).</span></span> <span data-ttu-id="623ad-105">您也可以在使用 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)或/I 命令列選項安裝封裝時，在命令列上設定 **PATCH** 屬性。</span><span class="sxs-lookup"><span data-stu-id="623ad-105">You can also set the **PATCH** property on the command line while installing a package using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or the /i Command Line Option.</span></span>

<span data-ttu-id="623ad-106">**PATCH** 屬性的值是要安裝的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="623ad-106">The value of the **PATCH** property is a list of the patches that are being installed.</span></span> <span data-ttu-id="623ad-107">清單中的每個修補程式都會以修補程式套件 ( .msp 檔案的完整路徑來表示。 ) 清單中的完整路徑會以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="623ad-107">Each patch in the list is represented by the full path to the patch's package (.msp file.) The full paths in the list are separated by semicolons.</span></span>

<span data-ttu-id="623ad-108">**Windows Installer 2.0：** 不支援多個修補程式。</span><span class="sxs-lookup"><span data-stu-id="623ad-108">**Windows Installer 2.0:** Multiple patches are not supported.</span></span> <span data-ttu-id="623ad-109">需要 Windows Installer 3.0 才能套用多個修補程式。</span><span class="sxs-lookup"><span data-stu-id="623ad-109">Windows Installer 3.0 is required to apply multiple patches.</span></span>

## <a name="remarks"></a><span data-ttu-id="623ad-110">備註</span><span class="sxs-lookup"><span data-stu-id="623ad-110">Remarks</span></span>

<span data-ttu-id="623ad-111">如果您使用 [Msimsp.exe](msimsp-exe.md) 建立修補程式套件，而且 [Patchwiz.dll](patchwiz-dll.md) 可以指定在套用特定修補程式時，只執行一個動作或一個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="623ad-111">If you create a patch package using [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) you can specify that an action or a dialog box only run when a particular patch is being applied.</span></span> <span data-ttu-id="623ad-112">當您建立修補程式套件時（例如 test .msp），您會撰寫產品的升級映射和修補程式建立屬性檔。</span><span class="sxs-lookup"><span data-stu-id="623ad-112">When you create the patch package, for example test.msp, you author an upgraded image of the product and a patch creation properties file.</span></span> <span data-ttu-id="623ad-113">撰寫修補程式建立屬性檔時，您可以在 [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) 資料表的 MediaSrcPropName 欄位中輸入屬性名稱（例如 PATCHFORTEST）。</span><span class="sxs-lookup"><span data-stu-id="623ad-113">When authoring the patch creation properties file you can enter a property name, for example PATCHFORTEST, in the MediaSrcPropName field of the [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) table.</span></span> <span data-ttu-id="623ad-114">當您撰寫升級之產品影像的順序資料表時，可以在 sequence 資料表的 [條件] 資料行中，加入您想要進行條件化之動作或對話方塊的條件式語句。</span><span class="sxs-lookup"><span data-stu-id="623ad-114">When you author the sequence tables of the upgraded image of the product, you can include in the Condition column of the sequence table a conditional statement for the action or dialog box you want to make conditional.</span></span>

<span data-ttu-id="623ad-115">例如，您可以使用下列條件陳述式，只在套用了測試 .msp 時執行動作或對話方塊。</span><span class="sxs-lookup"><span data-stu-id="623ad-115">For example, you can use the following conditional statement to run an action or dialog box only when test.msp is being applied.</span></span>

<dl> <span data-ttu-id="623ad-116">修補程式和 PATCHFORTEST 和修補程式 >< PATCHFORTEST</span><span class="sxs-lookup"><span data-stu-id="623ad-116">PATCH AND PATCHFORTEST AND PATCH >< PATCHFORTEST</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="623ad-117">由於 **PATCH** 屬性可以包含多個修補程式，請使用 substring 運算子 "><" 來測試是否有特定的修補程式，而不是 equals 運算子 "="。</span><span class="sxs-lookup"><span data-stu-id="623ad-117">Because the **PATCH** property can contain multiple patches, use the substring operator "><" to test for the presence of a particular patch rather than the equals operator "=".</span></span> <span data-ttu-id="623ad-118">如需條件陳述式的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="623ad-118">For more information about conditional statements see the [Conditional Statement Syntax](conditional-statement-syntax.md) section.</span></span>

 

<span data-ttu-id="623ad-119">如果您套用包含 test .msp 的修補程式清單，安裝程式會設定這兩個屬性。</span><span class="sxs-lookup"><span data-stu-id="623ad-119">The installer sets both properties if you apply a list of patches that includes test.msp.</span></span> <span data-ttu-id="623ad-120">例如，您可以使用/p [命令列選項](command-line-options.md) 來套用兩個修補程式的清單。</span><span class="sxs-lookup"><span data-stu-id="623ad-120">For example, you can use the /p [Command Line Option](command-line-options.md) to apply a list of two patches.</span></span>

<span data-ttu-id="623ad-121">**msiexec/qb/p \\ \\ 臨時 \\ 臨時 \\ 臨時 \\ 修補程式 \\ 測試 .msp; \\ \\臨時 \\ \\ 的 XYZ \\ bar .msp**</span><span class="sxs-lookup"><span data-stu-id="623ad-121">**msiexec /qb /p \\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp**</span></span>

<span data-ttu-id="623ad-122">安裝程式會設定 **PATCH** 和 PATCHFORTEST 屬性，如下所示。</span><span class="sxs-lookup"><span data-stu-id="623ad-122">The installer sets the **PATCH** and PATCHFORTEST properties as follows.</span></span>

<dl> <span data-ttu-id="623ad-123">PATCH = \\ \\ 臨時 \\ 臨時 \\ \\ 的 XYZ 修補程式 \\ 測試 .msp; \\ \\臨時 \\ \\ 的 XYZ \\ bar .msp</span><span class="sxs-lookup"><span data-stu-id="623ad-123">PATCH=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp</span></span>  
<span data-ttu-id="623ad-124">PATCHFORTEST = \\ \\ 臨時 \\ 臨時 \\ \\ 的 XYZ 修補程式 \\ 測試 .msp</span><span class="sxs-lookup"><span data-stu-id="623ad-124">PATCHFORTEST=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp</span></span>  
</dl>

<span data-ttu-id="623ad-125">在此情況下，條件為 TRUE，而且上述條件式動作或對話方塊可以針對每個所安裝的修補程式、測試 .msp 和 .msp 執行。</span><span class="sxs-lookup"><span data-stu-id="623ad-125">In this case, the condition is TRUE and the above conditional action or dialog box can run for each patch being installed, test.msp and bar.msp.</span></span>

<span data-ttu-id="623ad-126">如果未套用 .msp，安裝程式就不會將它包含在 **PATCH** 屬性中，也不會設定 PATCHFORTEST。</span><span class="sxs-lookup"><span data-stu-id="623ad-126">If test.msp is not being applied, the installer does not include it in the **PATCH** property and does not set PATCHFORTEST.</span></span> <span data-ttu-id="623ad-127">在此情況下，上述條件為 FALSE，而條件式動作或對話方塊則不會執行。</span><span class="sxs-lookup"><span data-stu-id="623ad-127">In this case, the condition above is FALSE and the conditional action or dialog box does not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="623ad-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="623ad-128">Requirements</span></span>



| <span data-ttu-id="623ad-129">需求</span><span class="sxs-lookup"><span data-stu-id="623ad-129">Requirement</span></span> | <span data-ttu-id="623ad-130">值</span><span class="sxs-lookup"><span data-stu-id="623ad-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="623ad-131">版本</span><span class="sxs-lookup"><span data-stu-id="623ad-131">Version</span></span><br/> | <span data-ttu-id="623ad-132">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="623ad-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="623ad-133">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="623ad-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="623ad-134">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="623ad-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="623ad-135">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="623ad-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="623ad-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="623ad-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623ad-137">屬性</span><span class="sxs-lookup"><span data-stu-id="623ad-137">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="623ad-138">條件陳述式語法</span><span class="sxs-lookup"><span data-stu-id="623ad-138">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="623ad-139">條件陳述式語法的範例</span><span class="sxs-lookup"><span data-stu-id="623ad-139">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




