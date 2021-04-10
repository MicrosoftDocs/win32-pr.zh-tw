---
description: 語義類型的識別碼類型是其中一種文字格式類型。
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: 識別碼類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115365"
---
# <a name="identifier-type"></a><span data-ttu-id="116c3-103">識別碼類型</span><span class="sxs-lookup"><span data-stu-id="116c3-103">Identifier Type</span></span>

<span data-ttu-id="116c3-104">[語義類型](semantic-types.md)的識別碼類型是其中一種[文字格式類型](text-format-types.md)。</span><span class="sxs-lookup"><span data-stu-id="116c3-104">The Identifier Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="116c3-105">這個型別是由使用者以 Windows Installer [識別碼](identifier.md)的格式所提供的文字字串所組成。</span><span class="sxs-lookup"><span data-stu-id="116c3-105">This type consists of an text string provided by the user in the format of a Windows Installer [Identifier](identifier.md).</span></span> <span data-ttu-id="116c3-106">合併工具會將此字串取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)之 [值] 資料行中指定的範本。</span><span class="sxs-lookup"><span data-stu-id="116c3-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="116c3-107">若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入文字字串的名稱，在 [格式] 資料行中輸入 "0"，在 [類型] 資料行中輸入 "Identifier"，並將 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行保留空白。字串可能是與資料庫字碼頁相容的任何語言。</span><span class="sxs-lookup"><span data-stu-id="116c3-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Identifier" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="116c3-108">請參閱 [字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。</span><span class="sxs-lookup"><span data-stu-id="116c3-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="116c3-109">Null 是文字字串的有效值，除非 msmConfigItemNonNullable 已包含在 ModuleConfiguration 資料表的 Attributes 欄位中。</span><span class="sxs-lookup"><span data-stu-id="116c3-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



