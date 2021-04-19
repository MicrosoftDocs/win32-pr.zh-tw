---
description: FileSFPCatalog 資料表會將指定的檔案與系統檔案保護所使用的類別目錄檔案產生關聯。
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: FileSFPCatalog 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985676"
---
# <a name="filesfpcatalog-table"></a><span data-ttu-id="1e222-103">FileSFPCatalog 資料表</span><span class="sxs-lookup"><span data-stu-id="1e222-103">FileSFPCatalog Table</span></span>

<span data-ttu-id="1e222-104">FileSFPCatalog 資料表會將指定的檔案與系統檔案保護所使用的類別目錄檔案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="1e222-104">The FileSFPCatalog table associates specified files with the catalog files used by system file protection.</span></span>

<span data-ttu-id="1e222-105">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="1e222-105">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

<span data-ttu-id="1e222-106">FileSFPCatalog 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="1e222-106">The FileSFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="1e222-107">Column</span><span class="sxs-lookup"><span data-stu-id="1e222-107">Column</span></span>       | <span data-ttu-id="1e222-108">類型</span><span class="sxs-lookup"><span data-stu-id="1e222-108">Type</span></span>                         | <span data-ttu-id="1e222-109">答案</span><span class="sxs-lookup"><span data-stu-id="1e222-109">Key</span></span> | <span data-ttu-id="1e222-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="1e222-110">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="1e222-111">檔案\_</span><span class="sxs-lookup"><span data-stu-id="1e222-111">File\_</span></span>       | [<span data-ttu-id="1e222-112">識別碼</span><span class="sxs-lookup"><span data-stu-id="1e222-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="1e222-113">Y</span><span class="sxs-lookup"><span data-stu-id="1e222-113">Y</span></span>   | <span data-ttu-id="1e222-114">N</span><span class="sxs-lookup"><span data-stu-id="1e222-114">N</span></span>        |
| <span data-ttu-id="1e222-115">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="1e222-115">SFPCatalog\_</span></span> | [<span data-ttu-id="1e222-116">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="1e222-116">Filename</span></span>](filename.md)     | <span data-ttu-id="1e222-117">Y</span><span class="sxs-lookup"><span data-stu-id="1e222-117">Y</span></span>   | <span data-ttu-id="1e222-118">N</span><span class="sxs-lookup"><span data-stu-id="1e222-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1e222-119">資料行</span><span class="sxs-lookup"><span data-stu-id="1e222-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1e222-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="1e222-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="1e222-121">[File 資料表](file-table.md)的外鍵。</span><span class="sxs-lookup"><span data-stu-id="1e222-121">Foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e222-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="1e222-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span></span>
</dt> <dd>

<span data-ttu-id="1e222-123">[SFPCatalog 資料表](sfpcatalog-table.md)的外鍵。</span><span class="sxs-lookup"><span data-stu-id="1e222-123">Foreign key to the [SFPCatalog table](sfpcatalog-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e222-124">備註</span><span class="sxs-lookup"><span data-stu-id="1e222-124">Remarks</span></span>

<span data-ttu-id="1e222-125">[InstallSFPCatalogFile 動作](installsfpcatalogfile-action.md)會查詢[Component 資料表](component-table.md)、 [File Table](file-table.md)、FileSFPCatalog table 和[SFPCatalog 資料表](sfpcatalog-table.md)。</span><span class="sxs-lookup"><span data-stu-id="1e222-125">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), FileSFPCatalog table and [SFPCatalog table](sfpcatalog-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="1e222-126">驗證</span><span class="sxs-lookup"><span data-stu-id="1e222-126">Validation</span></span>

<dl>

[<span data-ttu-id="1e222-127">ICE03</span><span class="sxs-lookup"><span data-stu-id="1e222-127">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1e222-128">ICE06</span><span class="sxs-lookup"><span data-stu-id="1e222-128">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1e222-129">ICE32</span><span class="sxs-lookup"><span data-stu-id="1e222-129">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="1e222-130">ICE66</span><span class="sxs-lookup"><span data-stu-id="1e222-130">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="1e222-131">ICE76</span><span class="sxs-lookup"><span data-stu-id="1e222-131">ICE76</span></span>](ice76.md)  
</dl>

 

 



