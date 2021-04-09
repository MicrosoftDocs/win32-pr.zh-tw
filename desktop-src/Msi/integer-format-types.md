---
description: 可以在文字或整數資料庫欄位中使用可設定資料的整數格式類型。 MsmConfigItemNonNullable 屬性是此資料格式的隱含，不需要設定。 Null 對此類型而言永遠不是有效的值。
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: 整數格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693331"
---
# <a name="integer-format-types"></a><span data-ttu-id="cae33-105">整數格式類型</span><span class="sxs-lookup"><span data-stu-id="cae33-105">Integer Format Types</span></span>

<span data-ttu-id="cae33-106">可以在文字或整數資料庫欄位中使用可設定資料的整數格式類型。</span><span class="sxs-lookup"><span data-stu-id="cae33-106">The Integer Format Types of configurable data may be used in either text or integer database fields.</span></span> <span data-ttu-id="cae33-107">MsmConfigItemNonNullable 屬性是此資料格式的隱含，不需要設定。</span><span class="sxs-lookup"><span data-stu-id="cae33-107">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="cae33-108">Null 對此類型而言永遠不是有效的值。</span><span class="sxs-lookup"><span data-stu-id="cae33-108">Null is never a valid value for this type.</span></span>

<span data-ttu-id="cae33-109">下列整數格式類型存在。</span><span class="sxs-lookup"><span data-stu-id="cae33-109">The following Integer Format type exists.</span></span>

[<span data-ttu-id="cae33-110">任意整數類型</span><span class="sxs-lookup"><span data-stu-id="cae33-110">Arbitrary Integer Type</span></span>](arbitrary-integer-type.md)

<span data-ttu-id="cae33-111">整數格式類型的可設定專案會使用於文字或整數資料行，而且一般可以由任何正整數或負整數來取代。</span><span class="sxs-lookup"><span data-stu-id="cae33-111">Configurable items of the Integer Format Type are used in either text or integer columns and in general could be replaced by any positive or negative integer.</span></span> <span data-ttu-id="cae33-112">不過，特定可設定的專案也可能具有特性語義限制。</span><span class="sxs-lookup"><span data-stu-id="cae33-112">However, particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="cae33-113">例如，特定可設定的專案必須是介於0和100之間的整數，以及其他語義限制。</span><span class="sxs-lookup"><span data-stu-id="cae33-113">For example, a particular configurable item required to be an integer between 0 and 100 has and additional semantic restriction.</span></span> <span data-ttu-id="cae33-114">Mergemod.dll 不會強制執行這類限制，因此模組作者應該準備好處理任何符合指定整數格式類型的字串。</span><span class="sxs-lookup"><span data-stu-id="cae33-114">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Integer Format type.</span></span>

 

 



