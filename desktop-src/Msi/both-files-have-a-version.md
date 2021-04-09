---
description: 如果這兩個檔案都有版本號碼，Windows Installer 會使用下列流程圖所示的邏輯來判斷是否要取代屬於元件的所有已安裝檔案。
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: 這兩個檔案都有版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848946"
---
# <a name="both-files-have-a-version"></a><span data-ttu-id="284b0-103">這兩個檔案都有版本</span><span class="sxs-lookup"><span data-stu-id="284b0-103">Both Files Have a Version</span></span>

<span data-ttu-id="284b0-104">如果要安裝之元件的金鑰檔 (copy-A) 與已安裝在目標位置中的檔案具有相同的名稱 (copy-B) ，安裝程式會比較兩個檔案的版本號碼和語言。</span><span class="sxs-lookup"><span data-stu-id="284b0-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number and language of the two files.</span></span>

<span data-ttu-id="284b0-105">如果這兩個檔案都有版本號碼，則安裝程式會使用下列流程圖所示的邏輯，判斷是否要取代所有已安裝的檔案屬於元件。</span><span class="sxs-lookup"><span data-stu-id="284b0-105">If both files have a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="284b0-106">因為安裝程式只會安裝整個元件，所以如果已取代已安裝的金鑰檔，則會取代所有元件的檔案。</span><span class="sxs-lookup"><span data-stu-id="284b0-106">Because the installer only installs entire components, if the installed key file is replaced then all of the component's files are replaced.</span></span>

<span data-ttu-id="284b0-107">請注意，下圖說明預設檔案 [版本控制規則](file-versioning-rules.md)，可以藉由設定 [**REINSTALLMODE**](reinstallmode.md) 屬性來覆寫這些規則。</span><span class="sxs-lookup"><span data-stu-id="284b0-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="284b0-108">**REINSTALLMODE** 屬性的預設值為 "omus reinstall"。</span><span class="sxs-lookup"><span data-stu-id="284b0-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![當兩個檔案都有相同的名稱或版本號碼時，預設檔案版本控制規則](images/waiflow1.png)

<span data-ttu-id="284b0-110">上圖也可以搭配未指定語言的檔案使用。</span><span class="sxs-lookup"><span data-stu-id="284b0-110">The previous diagram can also be used with files with no language specified.</span></span> <span data-ttu-id="284b0-111">如果複製-A 具有指定的語言，而複製-B 沒有指定的語言，則會以複製-B 取代複製-B。</span><span class="sxs-lookup"><span data-stu-id="284b0-111">If copy-A has a specified language and copy-B has no specified language, copy-B is replaced with copy-A.</span></span> <span data-ttu-id="284b0-112">如果 copy A 和 copy-B 都未指定任何語言，則不會取代 copy B。</span><span class="sxs-lookup"><span data-stu-id="284b0-112">If copy-A and copy-B both have no language specified, then copy-B is not replaced.</span></span>

<span data-ttu-id="284b0-113">請參閱 [取代現有](replacing-existing-files.md)檔案的預設檔案版本控制範例。</span><span class="sxs-lookup"><span data-stu-id="284b0-113">See examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="284b0-114">這兩個檔案都沒有版本</span><span class="sxs-lookup"><span data-stu-id="284b0-114">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="284b0-115">這兩個檔案都沒有具有檔案雜湊檢查的版本</span><span class="sxs-lookup"><span data-stu-id="284b0-115">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="284b0-116">一個檔案有版本</span><span class="sxs-lookup"><span data-stu-id="284b0-116">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



