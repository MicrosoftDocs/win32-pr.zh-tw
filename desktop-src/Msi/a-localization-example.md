---
description: 此範例說明如何將安裝範例中所述的 Windows Installer 封裝當地語系化。 原始安裝套件會從英文變更為法文語言版本。
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: 當地語系化範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977045"
---
# <a name="a-localization-example"></a><span data-ttu-id="6bb90-104">當地語系化範例</span><span class="sxs-lookup"><span data-stu-id="6bb90-104">A Localization Example</span></span>

<span data-ttu-id="6bb90-105">此範例說明如何將 [安裝範例](an-installation-example.md)中所述的 Windows Installer 封裝當地語系化。</span><span class="sxs-lookup"><span data-stu-id="6bb90-105">This example illustrates how to localize the Windows Installer package described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="6bb90-106">原始安裝套件會從英文變更為法文語言版本。</span><span class="sxs-lookup"><span data-stu-id="6bb90-106">The original installation package is changed from an English into French language version.</span></span>

<span data-ttu-id="6bb90-107">當地語系化範例具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="6bb90-107">The localization sample has the following specifications:</span></span>

-   <span data-ttu-id="6bb90-108">應用程式 MNP2000 的安裝 UI 應該從英文變更為法文。</span><span class="sxs-lookup"><span data-stu-id="6bb90-108">The installation UI for the application MNP2000 should be changed from English to French.</span></span>
-   <span data-ttu-id="6bb90-109">法文版的 MNP2000 包含以法文語言撰寫 Readme.txt 和 Help.txt 檔案。</span><span class="sxs-lookup"><span data-stu-id="6bb90-109">The French version of MNP2000 includes Readme.txt and Help.txt files written in the French language.</span></span>
-   <span data-ttu-id="6bb90-110">法文版本包含法國的旅遊專員清單，可提供給 Red 公園的機票。</span><span class="sxs-lookup"><span data-stu-id="6bb90-110">The French version includes a list of travel agents in France that can provide tickets to Red Park Arena.</span></span> <span data-ttu-id="6bb90-111">這份清單 (以新檔案的形式提供，Fre.txt) 不是英文版的一部分。</span><span class="sxs-lookup"><span data-stu-id="6bb90-111">This list (provided as a new file, Fre.txt) is not a part of the English version.</span></span>

<span data-ttu-id="6bb90-112">當地語系化 [Windows Installer 套件](localizing-a-windows-installer-package.md)一節將說明當地語系化安裝的一般程式。</span><span class="sxs-lookup"><span data-stu-id="6bb90-112">The general procedure for localizing an installation is described in the section [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="6bb90-113">將英文版的 MNP2000.msi 以及 [規劃安裝](planning-the-installation.md) 中所述的所有來源檔案複製到新的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="6bb90-113">Copy the English version of MNP2000.msi and all the source files described in [Planning the Installation](planning-the-installation.md) into a new folder.</span></span> <span data-ttu-id="6bb90-114">將資料夾中 MNP2000.msi 的名稱變更為 MNPFren.msi。</span><span class="sxs-lookup"><span data-stu-id="6bb90-114">Change the name of the MNP2000.msi in the folder to MNPFren.msi.</span></span> <span data-ttu-id="6bb90-115">在下列各節中，您將修改此複本，以將應用程式當地語系化為法文。</span><span class="sxs-lookup"><span data-stu-id="6bb90-115">In the following sections you will modify this copy to localize the application into French.</span></span>

[<span data-ttu-id="6bb90-116">繼續</span><span class="sxs-lookup"><span data-stu-id="6bb90-116">Continue</span></span>](checking-the-installation-database-code-page.md)

 

 



