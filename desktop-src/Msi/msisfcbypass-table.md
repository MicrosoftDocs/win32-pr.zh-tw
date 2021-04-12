---
description: MsiSFCBypass 資料表所包含的檔案清單，會在檔案安裝在 Microsoft Windows Me 時略過 Windows 檔案保護。
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: MsiSFCBypass 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319911"
---
# <a name="msisfcbypass-table"></a><span data-ttu-id="9191c-103">MsiSFCBypass 資料表</span><span class="sxs-lookup"><span data-stu-id="9191c-103">MsiSFCBypass Table</span></span>

<span data-ttu-id="9191c-104">MsiSFCBypass 資料表所包含的檔案清單，會在檔案安裝在 Microsoft Windows Me 時略過 Windows 檔案保護。</span><span class="sxs-lookup"><span data-stu-id="9191c-104">The MsiSFCBypass Table contains a list of files that should bypass Windows File Protection when the files are installed on Microsoft Windows Me.</span></span>

<span data-ttu-id="9191c-105">MsiSFCBypass 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="9191c-105">The MsiSFCBypass Table has the following column.</span></span>



| <span data-ttu-id="9191c-106">Column</span><span class="sxs-lookup"><span data-stu-id="9191c-106">Column</span></span> | <span data-ttu-id="9191c-107">類型</span><span class="sxs-lookup"><span data-stu-id="9191c-107">Type</span></span>                         | <span data-ttu-id="9191c-108">答案</span><span class="sxs-lookup"><span data-stu-id="9191c-108">Key</span></span> | <span data-ttu-id="9191c-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="9191c-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="9191c-110">檔案\_</span><span class="sxs-lookup"><span data-stu-id="9191c-110">File\_</span></span> | [<span data-ttu-id="9191c-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="9191c-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="9191c-112">Y</span><span class="sxs-lookup"><span data-stu-id="9191c-112">Y</span></span>   | <span data-ttu-id="9191c-113">N</span><span class="sxs-lookup"><span data-stu-id="9191c-113">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9191c-114">資料行</span><span class="sxs-lookup"><span data-stu-id="9191c-114">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9191c-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="9191c-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="9191c-116">檔案 [資料表](file-table.md) 的外鍵，指定當檔案安裝在 windows Me 時應該略過 Windows 檔案保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="9191c-116">The foreign key to the [File Table](file-table.md) that specifies the file that should bypass Windows File Protection when the file is installed on Windows Me.</span></span>

</dd> </dl>

 

 



