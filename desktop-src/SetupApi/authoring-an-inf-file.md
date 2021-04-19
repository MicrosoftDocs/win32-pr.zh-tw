---
description: 為安裝應用程式撰寫 INF 檔案時，您也應該參考 INF 檔案格式，該檔案格式記載于 INF 檔案和 INF 檔案區段的一般指導方針，以及 Microsoft Windows 2000 驅動程式開發工具組的指示詞。
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: 撰寫 INF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970395"
---
# <a name="authoring-an-inf-file"></a><span data-ttu-id="80a81-103">撰寫 INF 檔案</span><span class="sxs-lookup"><span data-stu-id="80a81-103">Authoring an INF file</span></span>

<span data-ttu-id="80a81-104">為安裝應用程式撰寫 INF 檔案時，您也應該參考 INF 檔案格式，該檔案格式記載于 INF 檔案和 *inf 檔案區段* 的 *一般指導方針*，以及 Microsoft Windows 2000 驅動程式開發工具組的指示詞。</span><span class="sxs-lookup"><span data-stu-id="80a81-104">When authoring an INF file for a Setup application you should also refer to the INF file format documented in *General Guidelines for INF Files* and *INF File Sections and Directives* of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="80a81-105">針對安裝應用程式撰寫 INF 檔案時，請遵守下列規則。</span><span class="sxs-lookup"><span data-stu-id="80a81-105">When authoring INF files for a setup application adhere to the following rules.</span></span>

-   <span data-ttu-id="80a81-106">每個 INF 檔案中都需要 **版本** 區段。</span><span class="sxs-lookup"><span data-stu-id="80a81-106">A **Version** section is required in every INF file.</span></span>
-   <span data-ttu-id="80a81-107">區段的開頭必須是以方括弧括住的區段名稱 (\[ \]) 。</span><span class="sxs-lookup"><span data-stu-id="80a81-107">Sections must begin with the section name enclosed by square brackets (\[\]).</span></span>
-   <span data-ttu-id="80a81-108">**DestinationDirs**、 **SourceDisksFiles**、 **SourceDisksNames**、 **Strings** 和 **Version** 區段的名稱必須與區段型別相同。</span><span class="sxs-lookup"><span data-stu-id="80a81-108">Names of **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings**, and **Version** sections must be identical to the section type.</span></span> <span data-ttu-id="80a81-109">例如，使用 \[ DestinationDirs \] 。</span><span class="sxs-lookup"><span data-stu-id="80a81-109">For example use \[DestinationDirs\].</span></span> <span data-ttu-id="80a81-110">作者可以指定其他類型的區段名稱。</span><span class="sxs-lookup"><span data-stu-id="80a81-110">Authors may specify the names of other types of sections.</span></span>
-   <span data-ttu-id="80a81-111">**SourceDisksNames** 和 **SourceDisksFiles** 區段的名稱可以附加平臺特定的尾碼。</span><span class="sxs-lookup"><span data-stu-id="80a81-111">Names of **SourceDisksNames** and **SourceDisksFiles** sections may be appended with a platform-specific suffix.</span></span> <span data-ttu-id="80a81-112">例如，若要顯示 Intel 特定的 **SourceDisksNames** 區段，請使用 \[ SourceDisksNames。 \]</span><span class="sxs-lookup"><span data-stu-id="80a81-112">For example, to show an Intel-specific **SourceDisksNames** section use \[SourceDisksNames.x86\].</span></span> <span data-ttu-id="80a81-113">如果安裝函式找到符合使用者平臺的平臺特定 **SourceDisksNames** 和 **SourceDisksFiles** 區段，則這些函式會使用平臺特定區段。</span><span class="sxs-lookup"><span data-stu-id="80a81-113">If the setup functions find platform-specific **SourceDisksNames** and **SourceDisksFiles** sections matching the user's platform, the functions use the platform-specific sections.</span></span> <span data-ttu-id="80a81-114">否則，安裝程式函數會使用非尾碼的 **SourceDisksNames** 和 **SourceDisksFiles** 區段。</span><span class="sxs-lookup"><span data-stu-id="80a81-114">Otherwise the setup functions use the non-suffixed **SourceDisksNames** and **SourceDisksFiles** sections.</span></span> <span data-ttu-id="80a81-115">安裝函式可以用程式設計的方式決定使用者的系統。</span><span class="sxs-lookup"><span data-stu-id="80a81-115">The setup functions can programmatically determine the user's system.</span></span> <span data-ttu-id="80a81-116">請參閱 [INF SourceDisksNames 和 SourceDisksFiles 章節範例](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md)。</span><span class="sxs-lookup"><span data-stu-id="80a81-116">See the [INF SourceDisksNames and SourceDisksFiles Sections Example](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span></span>
-   <span data-ttu-id="80a81-117">值可以使用%*strkey*% 形式以可替換的字串表示。</span><span class="sxs-lookup"><span data-stu-id="80a81-117">Values may be expressed as replaceable strings using the form %*strkey*%.</span></span> <span data-ttu-id="80a81-118">若要在字串中使用% 字元，請使用%%。</span><span class="sxs-lookup"><span data-stu-id="80a81-118">To use a % character in the string, use %%.</span></span> <span data-ttu-id="80a81-119">Strkey 必須定義在 INF 檔案的 **字串** 區段中。</span><span class="sxs-lookup"><span data-stu-id="80a81-119">The strkey must be defined in a **Strings** section of the INF file.</span></span>

 

 



