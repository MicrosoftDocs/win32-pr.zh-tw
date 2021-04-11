---
description: '&\# 0034;位&\# 0034; 沒有內容要求的類型，使用者提供的整數值是用來設定位中的一或多個位。 這段文字可能是與資料庫字碼頁相容的任何語言。'
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: 任意位欄位類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115380"
---
# <a name="arbitrary-bitfield-type"></a><span data-ttu-id="8ec8d-104">任意位欄位類型</span><span class="sxs-lookup"><span data-stu-id="8ec8d-104">Arbitrary Bitfield Type</span></span>

<span data-ttu-id="8ec8d-105">沒有內容要求的 "bit" 類型，使用者提供的整數值是用來設定位中的一或多個位。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-105">The "Bitfield" type with no context requests that the user provide an integer whose value is used to set one or more bits in a bitfield.</span></span> <span data-ttu-id="8ec8d-106">這段文字可能是與資料庫字碼頁相容的任何語言。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-106">This text may be in any language compatible with the code page of the database.</span></span>

<span data-ttu-id="8ec8d-107">[語義類型](semantic-types.md)的任意位欄位類型是其中一個位欄位類型。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-107">The Arbitrary Bitfield Type of [semantic type](semantic-types.md) is one of the Bitfield Types.</span></span> <span data-ttu-id="8ec8d-108">此類型是由使用者從一組選擇所選擇的整數所組成。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-108">This type consists of an integer chosen by the user from a set of choices.</span></span> <span data-ttu-id="8ec8d-109">合併工具會將選取的整數取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中所指定的範本。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-109">The merge tool substitutes the selected integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="8ec8d-110">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入專案的名稱，在 [格式] 資料行中輸入 "3"，將類型資料行保留空白，並在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入可能的整數清單。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-110">To specify a configurable item of this type, module authors should enter the name of the item into the Name column, enter "3" into the Format column, leave the Type column blank, and enter the list of possible integers in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="8ec8d-111">類型資料行是保留的，而且必須是 null。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-111">The Type column is reserved and must be null.</span></span> <span data-ttu-id="8ec8d-112">所有欄位類型的 CoNtextData 資料行中的專案都必須採用 ";" 格式 <mask> 。<Name>=</span><span class="sxs-lookup"><span data-stu-id="8ec8d-112">The entry in the ContextData column for all Bitfield Format types must be in the form "<mask>;<Name>=</span></span><value><span data-ttu-id="8ec8d-113">;<Name>=</span><span class="sxs-lookup"><span data-stu-id="8ec8d-113">;<Name>=</span></span><value><span data-ttu-id="8ec8d-114">... "，其中 <mask> 是一個整數值，指出感興趣的位、 <Name> 可當地語系化的顯示名稱，以及</span><span class="sxs-lookup"><span data-stu-id="8ec8d-114">....", where <mask> is an integer value indicating the bits of interest, <Name> is a localizable display name for the choice, and</span></span> <value> <span data-ttu-id="8ec8d-115">這是十進位整數值。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-115">is a decimal integer value.</span></span> <span data-ttu-id="8ec8d-116">內容資料行使用中的 [CMSM 特殊格式](cmsm-special-format.md) 和所有等位類型。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-116">The context column is in use [CMSM Special Format](cmsm-special-format.md) and for all bitfield types.</span></span> <span data-ttu-id="8ec8d-117">您可以在欄位中輸入常值 "=" 或 ";" 字元，方法是在 <Name> 該字元前面加上反斜線 ( ' \\ ' ) 字元。</span><span class="sxs-lookup"><span data-stu-id="8ec8d-117">A literal "=" or ";" character can be entered in the <Name> field by prefixing it with a backslash ('\\') character.</span></span>

 

 



