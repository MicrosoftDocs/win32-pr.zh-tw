---
description: 如果只有其中一個檔案有版本號碼，Windows Installer 會使用下列流程圖所示的邏輯來判斷是否要取代屬於元件的所有已安裝檔案。
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: 一個檔案有版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114168"
---
# <a name="one-file-has-a-version"></a><span data-ttu-id="de681-103">一個檔案有版本</span><span class="sxs-lookup"><span data-stu-id="de681-103">One File Has a Version</span></span>

<span data-ttu-id="de681-104">如果要安裝之元件的金鑰檔 (copy-A) 與已安裝在目標位置中的檔案具有相同的名稱 (copy-B) ，安裝程式會比較兩個檔案的版本號碼、日期和語言。</span><span class="sxs-lookup"><span data-stu-id="de681-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="de681-105">如果只有其中一個檔案有版本號碼，則安裝程式會使用下列流程圖所示的邏輯來判斷是否要取代屬於該元件的所有已安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="de681-105">If only one of the files has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="de681-106">因為安裝程式只會安裝整個元件，所以如果已取代已安裝的金鑰檔，則會取代所有元件的檔案。</span><span class="sxs-lookup"><span data-stu-id="de681-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="de681-107">請注意，下圖說明預設檔案 [版本控制規則](file-versioning-rules.md)，可以藉由設定 [**REINSTALLMODE**](reinstallmode.md) 屬性來覆寫這些規則。</span><span class="sxs-lookup"><span data-stu-id="de681-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="de681-108">**REINSTALLMODE** 屬性的預設值為 "omus reinstall"。</span><span class="sxs-lookup"><span data-stu-id="de681-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![只有一個檔案有版本號碼時的預設檔案版本控制規則](images/waiflow3.png)

<span data-ttu-id="de681-110">請參閱 [取代現有](replacing-existing-files.md)檔案的預設檔案版本控制範例。</span><span class="sxs-lookup"><span data-stu-id="de681-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="de681-111">這兩個檔案都有版本</span><span class="sxs-lookup"><span data-stu-id="de681-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="de681-112">這兩個檔案都沒有版本</span><span class="sxs-lookup"><span data-stu-id="de681-112">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="de681-113">這兩個檔案都沒有具有檔案雜湊檢查的版本</span><span class="sxs-lookup"><span data-stu-id="de681-113">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)

 

 



