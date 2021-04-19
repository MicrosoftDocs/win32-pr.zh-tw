---
description: 封包是單一檔案（通常副檔名為 .cab），可將壓縮檔案儲存在檔案庫中。
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: 封包檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996698"
---
# <a name="cabinet-files"></a><span data-ttu-id="c544c-103">封包檔</span><span class="sxs-lookup"><span data-stu-id="c544c-103">Cabinet Files</span></span>

<span data-ttu-id="c544c-104">封包是單一檔案（通常副檔名為 .cab），可將壓縮檔案儲存在檔案庫中。</span><span class="sxs-lookup"><span data-stu-id="c544c-104">A cabinet is a single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="c544c-105">封包格式是封裝多個檔案的有效方式，因為壓縮會跨檔案界限執行，如此可大幅改善壓縮率。</span><span class="sxs-lookup"><span data-stu-id="c544c-105">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, which significantly improves the compression ratio.</span></span>

<span data-ttu-id="c544c-106">開發人員可以使用封包檔建立工具（例如 Makecab.exe）製作封包檔，以與安裝程式套件搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c544c-106">Developers can use a cabinet file creation tool such as Makecab.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="c544c-107">Makecab.exe 公用程式包含在 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中。</span><span class="sxs-lookup"><span data-stu-id="c544c-107">The Makecab.exe utility is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="c544c-108">開發人員也可以使用封包檔建立工具（例如 Cabarc.exe）製作封包檔，以與安裝程式套件搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c544c-108">Developers can also use a cabinet file creation tool such as Cabarc.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="c544c-109">此工具會寫入鑽石封包結構。</span><span class="sxs-lookup"><span data-stu-id="c544c-109">This tool writes to the Diamond cabinet structure.</span></span>

<span data-ttu-id="c544c-110">封包檔內儲存之檔案的檔案索引鍵必須與檔案 [資料表](file-table.md) 的 file 資料行中的專案相符，而且封包中的檔案順序必須符合 [順序] 資料行中指定的檔案順序。</span><span class="sxs-lookup"><span data-stu-id="c544c-110">The file keys of the files stored inside of a cabinet file must match the entries in the File column of the [File table](file-table.md) and the sequence of files in the cabinet must match the file sequence specified in the Sequence column.</span></span> <span data-ttu-id="c544c-111">如需詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="c544c-111">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="c544c-112">大型檔案可以分割成兩個或多個封包檔。</span><span class="sxs-lookup"><span data-stu-id="c544c-112">Large files can be split between two or more cabinet files.</span></span> <span data-ttu-id="c544c-113">在下一個封包檔中，任何一個封包檔中都不能有15個以上的檔案。</span><span class="sxs-lookup"><span data-stu-id="c544c-113">There can be no more than 15 files in any one cabinet file that spans to the next cabinet file.</span></span> <span data-ttu-id="c544c-114">例如，如果您有三個封包檔，則第一個封包可以有15個檔案跨越第二個封包檔，而第二個封包檔可以有15個檔案跨越第三封封包檔。</span><span class="sxs-lookup"><span data-stu-id="c544c-114">For example, if you have three cabinet files the first cabinet can have 15 files that span to the second cabinet file and the second cabinet file can have 15 files that span to the third cabinet file.</span></span>

<span data-ttu-id="c544c-115">安裝程式會根據安裝所需的封包解壓縮檔案，並依照儲存在封包檔中的相同順序來安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="c544c-115">The installer extracts files from a cabinet as they are needed by the installation and installs them in the same order as they are stored in the cabinet file.</span></span> <span data-ttu-id="c544c-116">安裝封包中儲存之檔案的空間需求與安裝未壓縮檔案的空間需求不同。</span><span class="sxs-lookup"><span data-stu-id="c544c-116">The space requirements for installing a file stored in a cabinet are no different than for installing an uncompressed file.</span></span>

<span data-ttu-id="c544c-117">封包檔可以位於 .msi 檔案的內部或外部。</span><span class="sxs-lookup"><span data-stu-id="c544c-117">A cabinet file can be located inside or outside of the .msi file.</span></span> <span data-ttu-id="c544c-118">從在 Windows 7 或 Windows Server 2008 R2 上執行的 Windows Installer 5.0 開始，安裝程式會先儲存任何內嵌在 .msi 檔案中的封包，再快取安裝套件。</span><span class="sxs-lookup"><span data-stu-id="c544c-118">Beginning with Windows Installer 5.0 running on Windows 7 or Windows Server 2008 R2 the installer saves any cabinets that are embedded in the .msi file before caching the installation package.</span></span>

<span data-ttu-id="c544c-119">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 為了節省磁碟空間，安裝程式一律會移除任何內嵌在 .msi 檔案中的封包，然後才在使用者的電腦上快取安裝套件。</span><span class="sxs-lookup"><span data-stu-id="c544c-119">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** To conserve disk space, the installer always removes any cabinets that are embedded in the .msi file before caching the installation package on the user's computer.</span></span>

 

 



