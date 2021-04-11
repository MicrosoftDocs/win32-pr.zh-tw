---
description: 識別碼會指定資料行的名稱， (有時稱為屬性) 、目錄和別名。
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: 識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112424"
---
# <a name="identifiers"></a><span data-ttu-id="3e5c7-103">識別碼</span><span class="sxs-lookup"><span data-stu-id="3e5c7-103">Identifiers</span></span>

<span data-ttu-id="3e5c7-104">識別碼會指定資料行的名稱， (有時稱為屬性) 、目錄和別名。</span><span class="sxs-lookup"><span data-stu-id="3e5c7-104">Identifiers specify the names of columns (sometimes referred to as properties), catalogs, and aliases.</span></span> <span data-ttu-id="3e5c7-105">例如，DateCreated 是兩個系統定義的屬性資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e5c7-105">For example, System.ItemName and System.DateCreated are the identifiers of two system-defined property columns.</span></span> <span data-ttu-id="3e5c7-106">相反地，常值會指定字串和數值。</span><span class="sxs-lookup"><span data-stu-id="3e5c7-106">Literals, by contrast, specify string and numeric values.</span></span>


<span data-ttu-id="3e5c7-107">您可以建立長度最多為128個字元的識別碼，並以兩種類型的其中一種，以識別碼名稱中使用的字元來區分：</span><span class="sxs-lookup"><span data-stu-id="3e5c7-107">You can create identifiers that are up to 128 characters long, and in one of two types, distinguished by the characters used in the identifier name:</span></span>

-   <span data-ttu-id="3e5c7-108">**一般識別碼** 只會包含字元 a-z、a-z、0-9、底線 (\_) 和點 (. ) ，並且以字母開頭。</span><span class="sxs-lookup"><span data-stu-id="3e5c7-108">**Regular identifiers** contain only the characters A-Z, a-z, 0-9, underscore (\_), and dot (.), and they begin with a letter.</span></span> <span data-ttu-id="3e5c7-109">您不需要用雙引號括住一般識別碼 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="3e5c7-109">You do not need to enclose regular identifiers in double quotation marks (" ").</span></span>
-   <span data-ttu-id="3e5c7-110">**分隔識別碼** 可以包含任何有效的 Unicode 字元，而且必須用雙引號括住。</span><span class="sxs-lookup"><span data-stu-id="3e5c7-110">**Delimited identifiers** can contain any valid Unicode character and must be enclosed in double quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="3e5c7-111">在 FREETEXT 和 CONTAINS 子句中， \* 當您想要指定 Windows Search 包含查詢中的所有索引屬性時，您可以使用星號 () 作為特殊的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e5c7-111">In FREETEXT and CONTAINS clauses, you can use the asterisk (\*) as a special column identifier when you want to specify that Windows Search includes all of the indexed properties in the query.</span></span> <span data-ttu-id="3e5c7-112">雖然它不是一般識別碼，但不需要使用雙引號。</span><span class="sxs-lookup"><span data-stu-id="3e5c7-112">Although it is not a regular identifier, it does not require double quotation marks.</span></span>

 

 

 



