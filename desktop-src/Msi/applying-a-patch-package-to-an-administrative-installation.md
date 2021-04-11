---
description: 您可以藉由安裝在產生 Patch 套件中建立的範例 patch MNP2000，將小更新套用至 MNP2000.msi 的系統管理來源映射。
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: 將修補套件套用至系統管理安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944032"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a><span data-ttu-id="fdc31-103">將修補套件套用至系統管理安裝</span><span class="sxs-lookup"><span data-stu-id="fdc31-103">Applying a Patch Package to an Administrative Installation</span></span>

<span data-ttu-id="fdc31-104">您可以藉由安裝在 [產生 Patch 套件](generating-a-patch-package.md)中建立的範例 patch MNP2000，將小更新套用至 MNP2000.msi 的系統管理來源映射。</span><span class="sxs-lookup"><span data-stu-id="fdc31-104">You may apply the small update to an administrative source image of MNP2000.msi by installing the sample patch MNP2000.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="fdc31-105">然後，您可以要求使用者從新的系統管理來源映射重新安裝應用程式，以將更新傳播給使用者。</span><span class="sxs-lookup"><span data-stu-id="fdc31-105">The update can then be propagated to users by requesting that they reinstall the application from the new administrative source image.</span></span>

<span data-ttu-id="fdc31-106">系統管理員可以使用下列命令列，將位於//server/MNP2000.msi 的系統管理來源映射更新為新的來源映射，此映射與系統管理安裝從完整更新的 CD-ROM 產生的不同。</span><span class="sxs-lookup"><span data-stu-id="fdc31-106">An administrator can use the following command line to update the administrative source image located at //server/MNP2000.msi to a new source image that is the same as would be produced by an administrative installation from a fully updated CD-ROM.</span></span>

<span data-ttu-id="fdc31-107">**msiexec/a//server/MNP2000.msi/p MNP2000 .msp**</span><span class="sxs-lookup"><span data-stu-id="fdc31-107">**msiexec /a //server/MNP2000.msi /p MNP2000.msp**</span></span>

<span data-ttu-id="fdc31-108">使用 MNP2000 的工作組成員必須從新的系統管理來源映射重新安裝應用程式，才能接收更新。</span><span class="sxs-lookup"><span data-stu-id="fdc31-108">Members of the workgroup using MNP2000 then must reinstall the application from the new administrative source image to receive the update.</span></span>

<span data-ttu-id="fdc31-109">若要完全重新安裝應用程式，並在使用者的電腦上快取更新的 .msi 檔案，使用者可以輸入下列其中一個命令。</span><span class="sxs-lookup"><span data-stu-id="fdc31-109">To completely reinstall the applications and cache the updated .msi file on the user's computer, users may enter either of the following commands.</span></span>

<span data-ttu-id="fdc31-110">**msiexec/fvomus//server/MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="fdc31-110">**msiexec /fvomus //server/MNP2000.msi**</span></span>

<span data-ttu-id="fdc31-111">**msiexec/I//server/MNP2000.msi 重新安裝 = ALL REINSTALLMODE = vomus reinstall**</span><span class="sxs-lookup"><span data-stu-id="fdc31-111">**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**</span></span>

<span data-ttu-id="fdc31-112">若只要重新安裝已更新的協同功能，並在使用者的電腦上快取更新的 .msi 檔案，則使用者可以輸入下列命令。</span><span class="sxs-lookup"><span data-stu-id="fdc31-112">To reinstall only the updated Concert feature and cache the updated .msi file on the user's computer, users may enter the following command.</span></span>

<span data-ttu-id="fdc31-113">**msiexec/I//server/MNP2000.msi 重新安裝 = 協同 REINSTALLMODE = vomus reinstall**</span><span class="sxs-lookup"><span data-stu-id="fdc31-113">**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**</span></span>

## <a name="next-example"></a><span data-ttu-id="fdc31-114">下一個範例</span><span class="sxs-lookup"><span data-stu-id="fdc31-114">Next example</span></span>

[<span data-ttu-id="fdc31-115">當地語系化範例</span><span class="sxs-lookup"><span data-stu-id="fdc31-115">A Localization Example</span></span>](a-localization-example.md)

 

 



