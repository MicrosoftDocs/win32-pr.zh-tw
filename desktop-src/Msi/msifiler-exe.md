---
description: MsiFiler.exe 會根據來原始目錄，在檔案資料表中填入檔案版本、語言和大小。 它也可以使用檔案雜湊來更新 MsiFileHash 資料表。
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991709"
---
# <a name="msifilerexe"></a><span data-ttu-id="915ef-104">Msifiler.exe</span><span class="sxs-lookup"><span data-stu-id="915ef-104">Msifiler.exe</span></span>

<span data-ttu-id="915ef-105">MsiFiler.exe 會根據來原始目錄，在檔案 [資料表](file-table.md) 中填入檔案版本、語言和大小。</span><span class="sxs-lookup"><span data-stu-id="915ef-105">MsiFiler.exe populates the [File table](file-table.md) with file versions, languages, and sizes based upon a source directory.</span></span> <span data-ttu-id="915ef-106">它也可以使用檔案雜湊來更新 [MsiFileHash 資料表](msifilehash-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="915ef-106">It can also update the [MsiFileHash table](msifilehash-table.md) with file hashes.</span></span>

## <a name="syntax"></a><span data-ttu-id="915ef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="915ef-107">Syntax</span></span>

<span data-ttu-id="915ef-108">**msifiler.exe-d** *{database}* **\[ -v \] \[ -h \] \[ -s ALTSOURCE \]**</span><span class="sxs-lookup"><span data-stu-id="915ef-108">**msifiler.exe -d** *{database}* **\[-v\] \[-h\] \[-s ALTSOURCE\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="915ef-109">命令列選項</span><span class="sxs-lookup"><span data-stu-id="915ef-109">Command Line Options</span></span>

<span data-ttu-id="915ef-110">Msifiler.exe 會使用下列不區分大小寫的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="915ef-110">Msifiler.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="915ef-111">斜線分隔符號也可以用來取代虛線。</span><span class="sxs-lookup"><span data-stu-id="915ef-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="915ef-112">選項</span><span class="sxs-lookup"><span data-stu-id="915ef-112">Option</span></span> | <span data-ttu-id="915ef-113">參數</span><span class="sxs-lookup"><span data-stu-id="915ef-113">Parameter</span></span>   | <span data-ttu-id="915ef-114">Description</span><span class="sxs-lookup"><span data-stu-id="915ef-114">Description</span></span>                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="915ef-115">-d</span><span class="sxs-lookup"><span data-stu-id="915ef-115">-d</span></span>     | <span data-ttu-id="915ef-116">*database*</span><span class="sxs-lookup"><span data-stu-id="915ef-116">*database*</span></span>  | <span data-ttu-id="915ef-117">要更新的資料庫 ( .msi 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="915ef-117">The database (.msi file) that is to be updated.</span></span>                                                                                                                              |
| <span data-ttu-id="915ef-118">-v</span><span class="sxs-lookup"><span data-stu-id="915ef-118">-v</span></span>     |             | <span data-ttu-id="915ef-119">使用詳細資訊模式。</span><span class="sxs-lookup"><span data-stu-id="915ef-119">Use verbose mode.</span></span>                                                                                                                                                            |
| <span data-ttu-id="915ef-120">-H</span><span class="sxs-lookup"><span data-stu-id="915ef-120">-h</span></span>     |             | <span data-ttu-id="915ef-121">填入 [MsiFileHash 資料表](msifilehash-table.md)。</span><span class="sxs-lookup"><span data-stu-id="915ef-121">Populate the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="915ef-122">如果資料表不存在，就會建立資料表。</span><span class="sxs-lookup"><span data-stu-id="915ef-122">This creates the table if it does not already exist.</span></span> <span data-ttu-id="915ef-123">MsiFileHash 資料表只能搭配未建立版本檔使用。</span><span class="sxs-lookup"><span data-stu-id="915ef-123">The MsiFileHash table can only be used with unversioned files.</span></span> |
| <span data-ttu-id="915ef-124">-S</span><span class="sxs-lookup"><span data-stu-id="915ef-124">-s</span></span>     | <span data-ttu-id="915ef-125">*ALTSOURCE*</span><span class="sxs-lookup"><span data-stu-id="915ef-125">*ALTSOURCE*</span></span> | <span data-ttu-id="915ef-126">ALTSOURCE 會指定用來尋找檔案的替代目錄。</span><span class="sxs-lookup"><span data-stu-id="915ef-126">ALTSOURCE specifies an alternative directory to find the files.</span></span>                                                                                                              |



 

<span data-ttu-id="915ef-127">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="915ef-127">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="915ef-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="915ef-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="915ef-129">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="915ef-129">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="915ef-130">使用目錄資料表</span><span class="sxs-lookup"><span data-stu-id="915ef-130">Using the Directory Table</span></span>](using-the-directory-table.md)
</dt> <dt>

[<span data-ttu-id="915ef-131">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="915ef-131">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



