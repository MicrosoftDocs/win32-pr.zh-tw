---
description: 可以在文字欄位中使用可設定資料的索引鍵格式類型，在資料庫資料表中提供索引鍵。
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: 索引鍵格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970615"
---
# <a name="key-format-types"></a><span data-ttu-id="8520c-103">索引鍵格式類型</span><span class="sxs-lookup"><span data-stu-id="8520c-103">Key Format Types</span></span>

<span data-ttu-id="8520c-104">可以在文字欄位中使用可設定資料的索引鍵格式類型，在資料庫資料表中提供索引鍵。</span><span class="sxs-lookup"><span data-stu-id="8520c-104">The Key Format Types of configurable data may be used in text fields to provide a key into a database table.</span></span> <span data-ttu-id="8520c-105">MsmConfigItemNonNullable 屬性是此資料格式的隱含，不需要設定。</span><span class="sxs-lookup"><span data-stu-id="8520c-105">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="8520c-106">Null 對此類型而言永遠不是有效的值。</span><span class="sxs-lookup"><span data-stu-id="8520c-106">Null is never a valid value for this type.</span></span> <span data-ttu-id="8520c-107">所有索引鍵格式專案的回應都必須採用 [CMSM 的特殊格式](cmsm-special-format.md)。</span><span class="sxs-lookup"><span data-stu-id="8520c-107">Responses to all Key format items must be in [CMSM Special Format](cmsm-special-format.md).</span></span>

<span data-ttu-id="8520c-108">存在下列索引鍵格式類型：</span><span class="sxs-lookup"><span data-stu-id="8520c-108">The following Key Format types exist:</span></span>

[<span data-ttu-id="8520c-109">目錄類型</span><span class="sxs-lookup"><span data-stu-id="8520c-109">Directory Type</span></span>](directory-type.md)

[<span data-ttu-id="8520c-110">檔案類型</span><span class="sxs-lookup"><span data-stu-id="8520c-110">File Type</span></span>](file-type.md)

[<span data-ttu-id="8520c-111">屬性類型</span><span class="sxs-lookup"><span data-stu-id="8520c-111">Property Type</span></span>](property-type.md)

[<span data-ttu-id="8520c-112">對話方塊類型</span><span class="sxs-lookup"><span data-stu-id="8520c-112">Dialog Type</span></span>](dialog-type.md)

[<span data-ttu-id="8520c-113">二進位類型</span><span class="sxs-lookup"><span data-stu-id="8520c-113">Binary Type</span></span>](binary-type.md)

[<span data-ttu-id="8520c-114">圖示類型</span><span class="sxs-lookup"><span data-stu-id="8520c-114">Icon Type</span></span>](icon-type.md)

<span data-ttu-id="8520c-115">索引鍵格式類型的可設定專案會在文字資料行中用來提供資料庫索引鍵，而且一般可以由任何文字字串取代。</span><span class="sxs-lookup"><span data-stu-id="8520c-115">Configurable items of the Key Format Type are used in text columns to provide a database key and in general could be replaced by any text string.</span></span> <span data-ttu-id="8520c-116">個別類型可能會有其他語法限制，但是 Mergemod.dll 不會強制執行這些限制。</span><span class="sxs-lookup"><span data-stu-id="8520c-116">The individual types may have additional syntactic restrictions, but these restrictions are not enforced by Mergemod.dll.</span></span> <span data-ttu-id="8520c-117">特定可設定的專案也可能具有特性語義限制。</span><span class="sxs-lookup"><span data-stu-id="8520c-117">Particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="8520c-118">例如，可能需要特定的可設定專案成為 [二進位資料表](binary-table.md) 中包含點陣圖影像的資料列的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="8520c-118">For example, a particular configurable item may be required to be a key into the [Binary table](binary-table.md) to a row containing a bitmap image.</span></span> <span data-ttu-id="8520c-119">Mergemod.dll 不會強制執行這類限制，因此模組作者應該準備好處理任何符合指定之索引鍵格式類型的字串。</span><span class="sxs-lookup"><span data-stu-id="8520c-119">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Key Format type.</span></span> <span data-ttu-id="8520c-120">除非以語義意義或屬性另有指定，否則 null 是有效的回應。</span><span class="sxs-lookup"><span data-stu-id="8520c-120">Unless otherwise specified by semantic meaning or attributes, null is a valid response.</span></span>

 

 



