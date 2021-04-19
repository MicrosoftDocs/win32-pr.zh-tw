---
description: 語義類型的任意文字類型是其中一種文字格式類型。
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: 任意文字類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995831"
---
# <a name="arbitrary-text-type"></a><span data-ttu-id="a6d1f-103">任意文字類型</span><span class="sxs-lookup"><span data-stu-id="a6d1f-103">Arbitrary Text Type</span></span>

<span data-ttu-id="a6d1f-104">[語義類型](semantic-types.md)的任意文字類型是其中一種[文字格式類型](text-format-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a6d1f-104">The Arbitrary Text Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="a6d1f-105">此類型是由使用者提供之任何長度的任意文字字串所組成。</span><span class="sxs-lookup"><span data-stu-id="a6d1f-105">This type consists of an arbitrary text string of any length provided by the user.</span></span> <span data-ttu-id="a6d1f-106">合併工具會將此任一字元串取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中所指定的範本。</span><span class="sxs-lookup"><span data-stu-id="a6d1f-106">The merge tool substitutes this arbitrary string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="a6d1f-107">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "0"，並將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 Type 和 CoNtextData 資料行保留空白。任意文字字串可能是與資料庫字碼頁相容的任何語言。</span><span class="sxs-lookup"><span data-stu-id="a6d1f-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).The arbitrary text string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="a6d1f-108">如需詳細資料，請參閱 [字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。</span><span class="sxs-lookup"><span data-stu-id="a6d1f-108">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="a6d1f-109">Null 是文字字串的有效值，除非 msmConfigItemNonNullable 已包含在 ModuleConfiguration 資料表的 Attributes 欄位中。</span><span class="sxs-lookup"><span data-stu-id="a6d1f-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



