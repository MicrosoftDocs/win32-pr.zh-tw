---
description: 深入瞭解：資料行
title: 資料行
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114092"
---
# <a name="columns"></a><span data-ttu-id="d0491-103">資料行</span><span class="sxs-lookup"><span data-stu-id="d0491-103">Columns</span></span>


<span data-ttu-id="d0491-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d0491-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="columns"></a><span data-ttu-id="d0491-105">資料行</span><span class="sxs-lookup"><span data-stu-id="d0491-105">Columns</span></span>

<span data-ttu-id="d0491-106">您可以藉由呼叫 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) 或不使用一組初始的資料行來建立資料表，方法是呼叫 [JetCreateTable](./jetcreatetable-function.md)。</span><span class="sxs-lookup"><span data-stu-id="d0491-106">A table can be created either with an initial set of columns by calling [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or without an initial set of columns by calling [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="d0491-107">ESE 中的資料表最多可以包含127個固定長度的資料行、128個可變長度的資料行，以及64993標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="d0491-107">Tables in ESE can contain up to 127 fixed-length columns, 128 variable-length columns, and 64,993 tagged columns.</span></span> <span data-ttu-id="d0491-108">資料行是由其名稱和識別碼所識別，並可透過 [JetAddColumn](./jetaddcolumn-function.md)以動態方式新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="d0491-108">Columns are identified by their name and ID and can be dynamically added to the table with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="d0491-109">建立資料行時，會使用特定的資料類型和一組選擇性的屬性，例如資料行是否為固定長度或是否可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="d0491-109">Columns are created with a specific data type and an optional set of attributes, such as whether the column is fixed-length or whether it can be NULL or not.</span></span>

<span data-ttu-id="d0491-110">資料行的型別決定了可能儲存在資料行中的資料，以及資料行的許多屬性，包括其編制索引的順序。</span><span class="sxs-lookup"><span data-stu-id="d0491-110">The type of a column determines the data that may be stored in the column and many of the properties of the column, including its order for indexing.</span></span> <span data-ttu-id="d0491-111">ESE 支援各式各樣的資料行類型，範圍從1位到 2 GB (2146483647 ASCII 字元或 1073741823 Unicode 字元) 。</span><span class="sxs-lookup"><span data-stu-id="d0491-111">ESE supports a wide range of column types, ranging in size from 1 bit to 2 GB (2146483647 ASCII characters or 1073741823 Unicode characters).</span></span> <span data-ttu-id="d0491-112">如需 ESE 所支援之資料行資料類型的完整清單，請參閱 [JET_COLTYP](./jet-coltyp.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="d0491-112">For a complete list of the column data types supported by ESE, see the [JET_COLTYP](./jet-coltyp.md) topic.</span></span> <span data-ttu-id="d0491-113">下列主題將討論 ESE 所支援的一些資料行類型：</span><span class="sxs-lookup"><span data-stu-id="d0491-113">The topics below discuss a few of the columns types supported by ESE:</span></span>

  - [<span data-ttu-id="d0491-114">標記、固定和變數資料行</span><span class="sxs-lookup"><span data-stu-id="d0491-114">Tagged, Fixed and Variable Columns</span></span>](./tagged-fixed-and-variable-columns.md)

  - [<span data-ttu-id="d0491-115">版本、自動遞增和託管資料行</span><span class="sxs-lookup"><span data-stu-id="d0491-115">Version, Auto-Increment and Escrow Columns</span></span>](./version-auto-increment-and-escrow-columns.md)

  - [<span data-ttu-id="d0491-116">Long 值資料行</span><span class="sxs-lookup"><span data-stu-id="d0491-116">Long Value Columns</span></span>](./long-value-columns.md)

  - [<span data-ttu-id="d0491-117">多重值的稀疏資料行</span><span class="sxs-lookup"><span data-stu-id="d0491-117">Multi-Valued Sparse Columns</span></span>](./multi-valued-sparse-columns.md)

  - [<span data-ttu-id="d0491-118">使用者定義資料行</span><span class="sxs-lookup"><span data-stu-id="d0491-118">User Defined Columns</span></span>](./user-defined-columns.md)

  - [<span data-ttu-id="d0491-119">使用資料表中的資料行</span><span class="sxs-lookup"><span data-stu-id="d0491-119">Using Columns in a Table</span></span>](./using-columns-in-a-table.md)
