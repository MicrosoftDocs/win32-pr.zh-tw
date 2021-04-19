---
description: CCPSearch 資料表包含用於合規性檢查程式 (CCP) 的檔案簽章清單。 使用者的電腦上至少必須要有一個檔案，使用者才能符合該程式。
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: CCPSearch 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982378"
---
# <a name="ccpsearch-table"></a><span data-ttu-id="7b25d-104">CCPSearch 資料表</span><span class="sxs-lookup"><span data-stu-id="7b25d-104">CCPSearch Table</span></span>

<span data-ttu-id="7b25d-105">CCPSearch 資料表包含用於合規性檢查程式 (CCP) 的檔案簽章清單。</span><span class="sxs-lookup"><span data-stu-id="7b25d-105">The CCPSearch table contains the list of file signatures used for the Compliance Checking Program (CCP).</span></span> <span data-ttu-id="7b25d-106">使用者的電腦上至少必須要有一個檔案，使用者才能符合該程式。</span><span class="sxs-lookup"><span data-stu-id="7b25d-106">At least one of these files needs to be present on a user's computer for the user to be in compliance with the program.</span></span>

<span data-ttu-id="7b25d-107">CCPSearch 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="7b25d-107">The CCPSearch table has the following column.</span></span>



| <span data-ttu-id="7b25d-108">Column</span><span class="sxs-lookup"><span data-stu-id="7b25d-108">Column</span></span>      | <span data-ttu-id="7b25d-109">類型</span><span class="sxs-lookup"><span data-stu-id="7b25d-109">Type</span></span>                         | <span data-ttu-id="7b25d-110">答案</span><span class="sxs-lookup"><span data-stu-id="7b25d-110">Key</span></span> | <span data-ttu-id="7b25d-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="7b25d-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="7b25d-112">簽名\_</span><span class="sxs-lookup"><span data-stu-id="7b25d-112">Signature\_</span></span> | [<span data-ttu-id="7b25d-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="7b25d-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="7b25d-114">Y</span><span class="sxs-lookup"><span data-stu-id="7b25d-114">Y</span></span>   | <span data-ttu-id="7b25d-115">N</span><span class="sxs-lookup"><span data-stu-id="7b25d-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="7b25d-116">Column</span><span class="sxs-lookup"><span data-stu-id="7b25d-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="7b25d-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_</span><span class="sxs-lookup"><span data-stu-id="7b25d-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="7b25d-118">簽章代表唯一的檔案簽章 \_ ，而且也是簽章、 [](signature-table.md) [RegLocator](reglocator-table.md)、 [IniLocator](inilocator-table.md)、 [CompLocator](complocator-table.md)和[DrLocator](drlocator-table.md)資料表中的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="7b25d-118">The Signature\_ represents a unique file signature and is also the external key into the [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b25d-119">備註</span><span class="sxs-lookup"><span data-stu-id="7b25d-119">Remarks</span></span>

<span data-ttu-id="7b25d-120">當執行 [CCPSearch 動作](ccpsearch-action.md) 或 [RMCCPSearch 動作](rmccpsearch-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="7b25d-120">This table is referred to when the [CCPSearch action](ccpsearch-action.md) or the [RMCCPSearch action](rmccpsearch-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="7b25d-121">驗證</span><span class="sxs-lookup"><span data-stu-id="7b25d-121">Validation</span></span>

<dl>

[<span data-ttu-id="7b25d-122">ICE03</span><span class="sxs-lookup"><span data-stu-id="7b25d-122">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7b25d-123">ICE06</span><span class="sxs-lookup"><span data-stu-id="7b25d-123">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7b25d-124">ICE32</span><span class="sxs-lookup"><span data-stu-id="7b25d-124">ICE32</span></span>](ice32.md)  
</dl>

 

 



