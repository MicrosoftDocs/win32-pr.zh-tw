---
description: 除了先前章節討論的資訊之外，uisample.msi 也包含範例使用者介面的資料。
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: 匯入消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848251"
---
# <a name="importing-the-user-interface"></a><span data-ttu-id="f6921-103">匯入消費者介面</span><span class="sxs-lookup"><span data-stu-id="f6921-103">Importing the User Interface</span></span>

<span data-ttu-id="f6921-104">除了先前章節討論的資訊之外，uisample.msi 也包含範例使用者介面的資料。</span><span class="sxs-lookup"><span data-stu-id="f6921-104">In addition to information discussed in previous sections, uisample.msi also contains data for a sample user interface.</span></span> <span data-ttu-id="f6921-105">如果您將 uisample.msi 合併到匯 [入空白資料庫](importing-a-blank-database.md)區段中的 MNP2000.msi，則這項資訊也會出現在 MNP2000.msi 中。</span><span class="sxs-lookup"><span data-stu-id="f6921-105">If you merged uisample.msi into MNP2000.msi in the section [Importing a Blank Database](importing-a-blank-database.md), then this information is present in MNP2000.msi as well.</span></span> <span data-ttu-id="f6921-106">範例使用者介面的資訊如下表所示。</span><span class="sxs-lookup"><span data-stu-id="f6921-106">The information for the sample user interface is in the following tables.</span></span>

-   [<span data-ttu-id="f6921-107">ActionText 資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-107">ActionText table</span></span>](actiontext-table.md)
-   [<span data-ttu-id="f6921-108">二進位資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-108">Binary table</span></span>](binary-table.md)
-   [<span data-ttu-id="f6921-109">控制資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-109">Control table</span></span>](control-table.md)
-   [<span data-ttu-id="f6921-110">ControlEvent 資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-110">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="f6921-111">對話方塊資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-111">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="f6921-112">錯誤資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-112">Error table</span></span>](error-table.md)
-   [<span data-ttu-id="f6921-113">EventMapping 資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-113">EventMapping table</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="f6921-114">選項按鈕資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-114">RadioButton table</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="f6921-115">樣式表單</span><span class="sxs-lookup"><span data-stu-id="f6921-115">TextStyle table</span></span>](textstyle-table.md)
-   [<span data-ttu-id="f6921-116">UIText 資料表</span><span class="sxs-lookup"><span data-stu-id="f6921-116">UIText table</span></span>](uitext-table.md)

<span data-ttu-id="f6921-117">安裝程式隨附的資料庫編輯器 Orca 包含對話方塊預覽選項，可讓您用來預覽上表中的資料所指定之使用者介面的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f6921-117">The database editor Orca provided with the installer includes a dialog preview option that you can use to preview the dialogs of the user interface that is specified by the data in the above tables.</span></span>

<span data-ttu-id="f6921-118">MNP2000.msi 安裝套件範例現在已準備好進行封裝驗證。</span><span class="sxs-lookup"><span data-stu-id="f6921-118">The sample installation package MNP2000.msi is now ready for package validation.</span></span> <span data-ttu-id="f6921-119">在第一次嘗試安裝封裝之前，請一律在新的封裝上執行驗證。</span><span class="sxs-lookup"><span data-stu-id="f6921-119">Always run validation on a new package before attempting to install the package for the first time.</span></span> <span data-ttu-id="f6921-120">這會在驗證安裝範例中討論。</span><span class="sxs-lookup"><span data-stu-id="f6921-120">This is discussed in Validating the Installation Sample.</span></span>

<span data-ttu-id="f6921-121">如果您不想要在範例封裝中包含使用者介面，請省略或移除上述表格中的所有資訊，但不包括用來定義 [**DefaultUIFont**](defaultuifont.md)屬性) 所需的 [[樣式表單] 表格](textstyle-table.md) (。</span><span class="sxs-lookup"><span data-stu-id="f6921-121">If you do not want to include the user interface in the sample package, omit or remove the all information in the tables shown above except for the [TextStyle table](textstyle-table.md) (which is needed to define the [**DefaultUIFont**](defaultuifont.md) property).</span></span> <span data-ttu-id="f6921-122">您也應該從 [屬性資料表](property-table.md)中移除使用者介面屬性。</span><span class="sxs-lookup"><span data-stu-id="f6921-122">You should also remove user interface properties from the [Property Table](property-table.md).</span></span> <span data-ttu-id="f6921-123">記事本範例的屬性工作表（不含 UI）如下所示。</span><span class="sxs-lookup"><span data-stu-id="f6921-123">An example Property table for the Notepad sample, without a UI, is shown below.</span></span> <span data-ttu-id="f6921-124">如果您複製此範例，請不要重複使用表格中顯示的 Guid。</span><span class="sxs-lookup"><span data-stu-id="f6921-124">Do not reuse the GUIDs shown in the table if you copy this example.</span></span>

[<span data-ttu-id="f6921-125">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="f6921-125">Property Table</span></span>](property-table.md)



| <span data-ttu-id="f6921-126">屬性</span><span class="sxs-lookup"><span data-stu-id="f6921-126">Property</span></span>                                   | <span data-ttu-id="f6921-127">值</span><span class="sxs-lookup"><span data-stu-id="f6921-127">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="f6921-128">**DefaultUIFont**</span><span class="sxs-lookup"><span data-stu-id="f6921-128">**DefaultUIFont**</span></span>](defaultuifont.md)     | <span data-ttu-id="f6921-129">DlgFont8</span><span class="sxs-lookup"><span data-stu-id="f6921-129">DlgFont8</span></span>                               |
| [<span data-ttu-id="f6921-130">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="f6921-130">**INSTALLLEVEL**</span></span>](installlevel.md)       | <span data-ttu-id="f6921-131">3</span><span class="sxs-lookup"><span data-stu-id="f6921-131">3</span></span>                                      |
| [<span data-ttu-id="f6921-132">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="f6921-132">**LIMITUI**</span></span>](limitui.md)                 | <span data-ttu-id="f6921-133">1</span><span class="sxs-lookup"><span data-stu-id="f6921-133">1</span></span>                                      |
| [<span data-ttu-id="f6921-134">**製造商**</span><span class="sxs-lookup"><span data-stu-id="f6921-134">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="f6921-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="f6921-135">Microsoft</span></span>                              |
| [<span data-ttu-id="f6921-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="f6921-136">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="f6921-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="f6921-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> |
| [<span data-ttu-id="f6921-138">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="f6921-138">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="f6921-139">1033</span><span class="sxs-lookup"><span data-stu-id="f6921-139">1033</span></span>                                   |
| [<span data-ttu-id="f6921-140">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="f6921-140">**ProductName**</span></span>](productname.md)         | <span data-ttu-id="f6921-141">MNP2000</span><span class="sxs-lookup"><span data-stu-id="f6921-141">MNP2000</span></span>                                |
| [<span data-ttu-id="f6921-142">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="f6921-142">**ProductVersion**</span></span>](productversion.md)   | <span data-ttu-id="f6921-143">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="f6921-143">01.40.0000</span></span>                             |
| [<span data-ttu-id="f6921-144">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="f6921-144">**UpgradeCode**</span></span>](upgradecode.md)         | <span data-ttu-id="f6921-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="f6921-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> |



 

<span data-ttu-id="f6921-146">您可以從命令列或從程式安裝沒有使用者介面的封裝。</span><span class="sxs-lookup"><span data-stu-id="f6921-146">A package without a user interface can be installed from the command line or from a program.</span></span> <span data-ttu-id="f6921-147">若要從命令列安裝封裝，請使用 [命令列選項](command-line-options.md)中所述的方法。</span><span class="sxs-lookup"><span data-stu-id="f6921-147">To install a package from the command line use the methods described in [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="f6921-148">若要從程式安裝套件，請使用 [使用安裝程式函數](using-installer-functions.md)中所述的方法。</span><span class="sxs-lookup"><span data-stu-id="f6921-148">To install a package from a program use the methods described in [Using Installer Functions](using-installer-functions.md).</span></span> <span data-ttu-id="f6921-149">在第一次嘗試安裝新套件之前，請一律在新的封裝上執行驗證。</span><span class="sxs-lookup"><span data-stu-id="f6921-149">Always run validation on a new package before attempting to install a new package for the first time.</span></span>

[<span data-ttu-id="f6921-150">繼續</span><span class="sxs-lookup"><span data-stu-id="f6921-150">Continue</span></span>](validating-an-installation-database.md)

 

 



