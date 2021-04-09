---
description: 系統管理安裝會在網路上建立應用程式或產品的來源映射。
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: 藉由修補系統管理映射來套用小型更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944030"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a><span data-ttu-id="939f5-103">藉由修補系統管理映射來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="939f5-103">Applying Small Updates by Patching an Administrative Image</span></span>

<span data-ttu-id="939f5-104">[系統管理安裝](administrative-installation.md)會在網路上建立應用程式或產品的來源映射。</span><span class="sxs-lookup"><span data-stu-id="939f5-104">An [administrative installation](administrative-installation.md) creates a source image of an application or product on a network.</span></span> <span data-ttu-id="939f5-105">工作組中具有此系統管理映射存取權的使用者，可以從此來源安裝產品。</span><span class="sxs-lookup"><span data-stu-id="939f5-105">Users in a workgroup who have access to this administrative image can install the product from this source.</span></span> <span data-ttu-id="939f5-106">您可以透過兩個步驟來更新此工作組的應用程式：</span><span class="sxs-lookup"><span data-stu-id="939f5-106">Updating the application for this workgroup is done in two steps:</span></span>

-   <span data-ttu-id="939f5-107">首先，您可以將小型更新修補程式套用至系統管理映射。</span><span class="sxs-lookup"><span data-stu-id="939f5-107">First, the small update patch can be applied to the administrative image.</span></span>
-   <span data-ttu-id="939f5-108">其次，必須將小型更新中的變更傳播給使用者。</span><span class="sxs-lookup"><span data-stu-id="939f5-108">Second, the changes in the small update need to be propagated to the users.</span></span>

<span data-ttu-id="939f5-109">**將小型更新修補程式套用至系統管理映射**</span><span class="sxs-lookup"><span data-stu-id="939f5-109">**To apply a small update patch to an administrative image**</span></span>

1.  <span data-ttu-id="939f5-110">以 [修補程式套件](patch-packages.md)的形式取得 small update。</span><span class="sxs-lookup"><span data-stu-id="939f5-110">Obtain the small update in the form of a [patch package](patch-packages.md).</span></span> <span data-ttu-id="939f5-111">例如，名為 Patch 的小更新。</span><span class="sxs-lookup"><span data-stu-id="939f5-111">For example, the small update named Patch.msp.</span></span>
2.  <span data-ttu-id="939f5-112">取得系統管理映射的路徑。</span><span class="sxs-lookup"><span data-stu-id="939f5-112">Obtain the path to the administrative image.</span></span>
3.  <span data-ttu-id="939f5-113">從命令列使用：</span><span class="sxs-lookup"><span data-stu-id="939f5-113">From the command line use:</span></span>

    <span data-ttu-id="939f5-114">**msiexec/a** 系統 *\[ 管理映射的路徑 .msi file \]* **/p** *patch .msp*</span><span class="sxs-lookup"><span data-stu-id="939f5-114">**msiexec /a** *\[path to administrative image .msi file\]* **/p** *patch.msp*</span></span>

4.  <span data-ttu-id="939f5-115">這會更新系統管理映射的應用程式檔和 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="939f5-115">This updates the application files and the .msi file of the administrative image.</span></span> <span data-ttu-id="939f5-116">如需可搭配 Msiexec.exe 使用之選項的清單，請參閱 [命令列選項](command-line-options.md)。</span><span class="sxs-lookup"><span data-stu-id="939f5-116">For a list of the options that can be used with Msiexec.exe, see [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="939f5-117">Windows Installer 會自動判斷系統管理映射是否使用短檔案名，並設定 [**SHORTFILENAMES**](shortfilenames.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="939f5-117">Windows Installer automatically determines whether the administrative image is using short file names and sets the [**SHORTFILENAMES**](shortfilenames.md) property.</span></span>
5.  <span data-ttu-id="939f5-118">產生的系統管理映射與系統管理安裝所產生的系統管理映射相同，它是使用包含更新的完整產品 cd-rom。</span><span class="sxs-lookup"><span data-stu-id="939f5-118">The resulting administrative image is the same as that produced by an administrative installation using a full product CD-ROM that includes the update.</span></span> <span data-ttu-id="939f5-119">當新使用者從這個來源安裝應用程式時，他們會收到已更新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="939f5-119">When new users install the application from this source they receive the updated application.</span></span>

<span data-ttu-id="939f5-120">**將 small update 傳播至工作組**</span><span class="sxs-lookup"><span data-stu-id="939f5-120">**To propagate the small update to the workgroup**</span></span>

-   <span data-ttu-id="939f5-121">工作組的成員會使用藉 [由重新安裝產品來套用小型更新](applying-small-updates-by-reinstalling-the-product.md)中所述的程式，從系統管理映射重新安裝應用程式，以取得變更。</span><span class="sxs-lookup"><span data-stu-id="939f5-121">Members of the workgroup obtain the changes by reinstalling the application from the administrative image using the procedure described in [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md).</span></span>

 

 



