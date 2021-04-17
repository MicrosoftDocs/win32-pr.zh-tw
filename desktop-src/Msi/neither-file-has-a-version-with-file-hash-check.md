---
description: 檔案雜湊適用于 Windows Installer。 如需詳細資訊，請參閱 MsiGetFileHash 和 MsiFileHash 資料表。 MsiFileHash 資料表只能搭配未建立版本檔使用。
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: 這兩個檔案都沒有具有檔案雜湊檢查的版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512776"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a><span data-ttu-id="11cfd-105">這兩個檔案都沒有具有檔案雜湊檢查的版本</span><span class="sxs-lookup"><span data-stu-id="11cfd-105">Neither File Has a Version with File Hash Check</span></span>

<span data-ttu-id="11cfd-106">檔案雜湊適用于 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="11cfd-106">File hashing is available with Windows Installer.</span></span> <span data-ttu-id="11cfd-107">如需詳細資訊，請參閱 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 和 [MsiFileHash 資料表](msifilehash-table.md)。</span><span class="sxs-lookup"><span data-stu-id="11cfd-107">For more information, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="11cfd-108">MsiFileHash 資料表只能搭配未建立版本檔使用。</span><span class="sxs-lookup"><span data-stu-id="11cfd-108">The MsiFileHash table can only be used with unversioned files.</span></span>

<span data-ttu-id="11cfd-109">如果要安裝之元件的金鑰檔 (copy-A) 與已安裝在目標位置中的檔案具有相同的名稱 (copy-B) ，安裝程式會比較兩個檔案的版本號碼、日期和語言。</span><span class="sxs-lookup"><span data-stu-id="11cfd-109">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="11cfd-110">如果這兩個檔案都沒有版本號碼，則安裝程式會使用下列流程圖所示的邏輯，判斷是否要取代所有已安裝的檔案屬於元件。</span><span class="sxs-lookup"><span data-stu-id="11cfd-110">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="11cfd-111">因為安裝程式只會安裝整個元件，所以如果已取代已安裝的金鑰檔，則會取代所有元件的檔案。</span><span class="sxs-lookup"><span data-stu-id="11cfd-111">Because the installer only installs entire components, if the installed key file is replaced then, all of the component's files are replaced.</span></span>

<span data-ttu-id="11cfd-112">請注意，下圖說明預設檔案 [版本控制規則](file-versioning-rules.md)，可以藉由設定 [**REINSTALLMODE**](reinstallmode.md) 屬性來覆寫這些規則。</span><span class="sxs-lookup"><span data-stu-id="11cfd-112">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="11cfd-113">**REINSTALLMODE** 屬性的預設值為 "omus reinstall"。</span><span class="sxs-lookup"><span data-stu-id="11cfd-113">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![reinstallmode 屬性設定覆寫時的預設檔案版本控制規則](images/waiflow2b.png)

<span data-ttu-id="11cfd-115">請參閱 [取代現有](replacing-existing-files.md)檔案的預設檔案版本控制範例。</span><span class="sxs-lookup"><span data-stu-id="11cfd-115">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="11cfd-116">這兩個檔案都有版本</span><span class="sxs-lookup"><span data-stu-id="11cfd-116">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="11cfd-117">這兩個檔案都沒有版本</span><span class="sxs-lookup"><span data-stu-id="11cfd-117">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="11cfd-118">一個檔案有版本</span><span class="sxs-lookup"><span data-stu-id="11cfd-118">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



