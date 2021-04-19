---
description: 資料查詢是要求類別實例的 WQL 語句。 為了發出資料查詢，應用程式會呼叫 IWbemServices：： ExecQuery 或 IWbemServices：： ExecQueryAsync 方法。
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: 要求類別實例資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997206"
---
# <a name="requesting-class-instance-data"></a><span data-ttu-id="c9377-104">要求類別實例資料</span><span class="sxs-lookup"><span data-stu-id="c9377-104">Requesting Class Instance Data</span></span>

<span data-ttu-id="c9377-105">資料查詢是要求類別實例的 WQL 語句。</span><span class="sxs-lookup"><span data-stu-id="c9377-105">Data queries are WQL statements that request instances of classes.</span></span> <span data-ttu-id="c9377-106">為了發出資料查詢，應用程式會呼叫 [**IWbemServices：： ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) 或 [**Iwbemservices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="c9377-106">To issue a data query, applications call the [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) or [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method.</span></span>

<span data-ttu-id="c9377-107">下列語句會用來進行資料查詢：</span><span class="sxs-lookup"><span data-stu-id="c9377-107">The following statements are used to make data queries:</span></span>

-   [<span data-ttu-id="c9377-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="c9377-108">SELECT</span></span>](select-statement-for-data-queries.md)
-   [<span data-ttu-id="c9377-109">ASSOCIATORS OF</span><span class="sxs-lookup"><span data-stu-id="c9377-109">ASSOCIATORS OF</span></span>](associators-of-statement.md)
-   [<span data-ttu-id="c9377-110">的參考</span><span class="sxs-lookup"><span data-stu-id="c9377-110">REFERENCES OF</span></span>](references-of-statement.md)
-   [<span data-ttu-id="c9377-111">ISA</span><span class="sxs-lookup"><span data-stu-id="c9377-111">ISA</span></span>](isa-operator-for-data-queries.md)

<span data-ttu-id="c9377-112">WQL SELECT 語句是標準結構化查詢語言 (SQL)  (SQL) 語句來抓取資訊，其中包含一些 WQL 專屬的限制和延伸。</span><span class="sxs-lookup"><span data-stu-id="c9377-112">The WQL SELECT statement is the standard Structured Query Language (SQL) statement for retrieving information, with a few restrictions and extensions specific to WQL.</span></span> <span data-ttu-id="c9377-113">雖然 SQL SELECT 語句通常用於資料庫環境中，以從資料表中取出特定資料行，但是在 WMI 中使用 WQL SELECT 語句來取出單一類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c9377-113">Although the SQL SELECT statement is typically used in the database environment to retrieve particular columns from tables, the WQL SELECT statement is used in WMI to retrieve instances of a single class.</span></span> <span data-ttu-id="c9377-114">WQL 不支援跨多個類別的查詢。</span><span class="sxs-lookup"><span data-stu-id="c9377-114">WQL does not support queries across multiple classes.</span></span>

<span data-ttu-id="c9377-115">語句的 ASSOCIATORS OF 和參考是 WQL 專屬的，而且不是標準 SQL 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c9377-115">The ASSOCIATORS OF and REFERENCES OF statements are specific to WQL and are not part of standard SQL.</span></span> <span data-ttu-id="c9377-116">語句的 ASSOCIATORS OF 會抓取與特定來源類別實例相關聯的所有類別實例，而的參考則會抓取參考特定來源實例的所有實例。</span><span class="sxs-lookup"><span data-stu-id="c9377-116">The ASSOCIATORS OF statement retrieves all class instances that are associated with a particular source class instance, and REFERENCES OF retrieves all instances that refer to a particular source instance.</span></span> <span data-ttu-id="c9377-117">關聯是以 [關聯類別](declaring-an-association-class.md)的實例來表示。</span><span class="sxs-lookup"><span data-stu-id="c9377-117">Associations are represented by instances of an [association class](declaring-an-association-class.md).</span></span>

 

 



