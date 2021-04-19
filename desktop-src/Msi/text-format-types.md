---
description: 可設定資料的文字格式類型可以是任何長度的文字字串。 不允許內嵌的 null。
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: 文字格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976586"
---
# <a name="text-format-types"></a><span data-ttu-id="4bc79-104">文字格式類型</span><span class="sxs-lookup"><span data-stu-id="4bc79-104">Text Format Types</span></span>

<span data-ttu-id="4bc79-105">可設定資料的文字格式類型可以是任何長度的文字字串。</span><span class="sxs-lookup"><span data-stu-id="4bc79-105">The text format types of configurable data may be text strings of any length.</span></span> <span data-ttu-id="4bc79-106">不允許內嵌的 null。</span><span class="sxs-lookup"><span data-stu-id="4bc79-106">Embedded nulls are not allowed.</span></span>

<span data-ttu-id="4bc79-107">下列文字格式類型存在：</span><span class="sxs-lookup"><span data-stu-id="4bc79-107">The following Text Format types exist:</span></span>

[<span data-ttu-id="4bc79-108">任意文字</span><span class="sxs-lookup"><span data-stu-id="4bc79-108">Arbitrary Text</span></span>](arbitrary-text-type.md)

[<span data-ttu-id="4bc79-109">Rtf</span><span class="sxs-lookup"><span data-stu-id="4bc79-109">RTF</span></span>](rtf-type.md)

[<span data-ttu-id="4bc79-110">格式 化</span><span class="sxs-lookup"><span data-stu-id="4bc79-110">Formatted</span></span>](formatted-type.md)

[<span data-ttu-id="4bc79-111">列舉</span><span class="sxs-lookup"><span data-stu-id="4bc79-111">Enum</span></span>](enum-type.md)

[<span data-ttu-id="4bc79-112">識別碼類型</span><span class="sxs-lookup"><span data-stu-id="4bc79-112">Identifier Type</span></span>](identifier-type.md)

<span data-ttu-id="4bc79-113">文字格式類型的可設定專案會用於非二進位資料庫欄位，而且一般可以由任何長度的任何字串取代。</span><span class="sxs-lookup"><span data-stu-id="4bc79-113">Configurable items of the Text Format Type are used in non-binary database fields and in general could be replaced by any string of any length.</span></span> <span data-ttu-id="4bc79-114">不過，特定可設定的專案也有語義限制。</span><span class="sxs-lookup"><span data-stu-id="4bc79-114">However, particular configurable items also have semantic restrictions.</span></span> <span data-ttu-id="4bc79-115">例如，在特定資料表中必須是外鍵的可設定專案具有其他語義限制。</span><span class="sxs-lookup"><span data-stu-id="4bc79-115">For example, a configurable item that is required to be a foreign key into a specific table has additional semantic restrictions.</span></span> <span data-ttu-id="4bc79-116">Mergemod.dll 不會強制執行這類語義限制，因此模組作者應該準備好處理任何符合指定文字格式類型的字串。</span><span class="sxs-lookup"><span data-stu-id="4bc79-116">Such semantic restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Text Format type.</span></span>

 

 



