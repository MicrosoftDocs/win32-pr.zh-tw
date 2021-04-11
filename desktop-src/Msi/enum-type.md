---
description: 語義類型的列舉類型是其中一種文字格式類型。
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: 列舉類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943889"
---
# <a name="enum-type"></a><span data-ttu-id="fb84e-103">列舉類型</span><span class="sxs-lookup"><span data-stu-id="fb84e-103">Enum Type</span></span>

<span data-ttu-id="fb84e-104">[語義類型](semantic-types.md)的列舉類型是其中一種[文字格式類型](text-format-types.md)。</span><span class="sxs-lookup"><span data-stu-id="fb84e-104">The Enum Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="fb84e-105">此類型是由使用者從一組選擇所選擇的文字字串所組成。</span><span class="sxs-lookup"><span data-stu-id="fb84e-105">This type consists of a text string chosen by the user from a set of choices.</span></span> <span data-ttu-id="fb84e-106">合併工具會將選取的字串取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中指定的範本。</span><span class="sxs-lookup"><span data-stu-id="fb84e-106">The merge tool substitutes the selected string selected into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="fb84e-107">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "0"，在 [類型] 資料行中輸入 "Enum"，然後在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入可能的字串清單。</span><span class="sxs-lookup"><span data-stu-id="fb84e-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Enum" into the Type column, and enter the list of possible strings in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="fb84e-108">可能的字串清單必須以分號 deliminated 的字串清單形式提供。</span><span class="sxs-lookup"><span data-stu-id="fb84e-108">The list of possible strings must be provided as a list of strings deliminated by semicolons.</span></span> <span data-ttu-id="fb84e-109">每個選擇的格式都必須是 "Name = Value"。</span><span class="sxs-lookup"><span data-stu-id="fb84e-109">Each choice must be in the form "Name=Value".</span></span> <span data-ttu-id="fb84e-110">您可以在分號前面加上反斜線字元，以將常值分號加入至值。</span><span class="sxs-lookup"><span data-stu-id="fb84e-110">A literal semicolon can be added to the value by prefixing the semicolon with a backslash character.</span></span> <span data-ttu-id="fb84e-111">除非 msmConfigItemNonNullable 已包含在 ModuleConfiguration 資料表的 [屬性] 欄位中，否則 Null 是有效的值。</span><span class="sxs-lookup"><span data-stu-id="fb84e-111">Null is a valid value unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



