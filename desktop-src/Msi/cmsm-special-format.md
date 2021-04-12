---
description: 搭配可設定合併模組使用的某些值需要特殊的文字處理。
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: CMSM 特殊格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192108"
---
# <a name="cmsm-special-format"></a><span data-ttu-id="72d3e-103">CMSM 特殊格式</span><span class="sxs-lookup"><span data-stu-id="72d3e-103">CMSM Special Format</span></span>

<span data-ttu-id="72d3e-104">搭配可設定合併模組使用的某些值需要特殊的文字處理。</span><span class="sxs-lookup"><span data-stu-id="72d3e-104">Certain values used with configurable merge modules require special text handling.</span></span> <span data-ttu-id="72d3e-105">描述為「CMSM 特殊格式」的文字字串會將分號 (; ) 和 equals (=) 字元作為用戶端合併工具或 Mergemod.dll 所使用的保留字元。</span><span class="sxs-lookup"><span data-stu-id="72d3e-105">A text string described as being in "CMSM Special Format" treats the semicolon (;) and equals (=) characters as reserved characters used by the client merge tool or Mergemod.dll.</span></span>

<span data-ttu-id="72d3e-106">下列位置目前使用 CMSM 的特殊格式：</span><span class="sxs-lookup"><span data-stu-id="72d3e-106">CMSM Special format is currently used in the following locations:</span></span>

-   <span data-ttu-id="72d3e-107">[ModuleSubstitution 資料表](modulesubstitution-table.md)的資料列資料行。</span><span class="sxs-lookup"><span data-stu-id="72d3e-107">The Row column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="72d3e-108">[ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行。</span><span class="sxs-lookup"><span data-stu-id="72d3e-108">The Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="72d3e-109">當位在 Format 資料行中的值時， [ModuleConfiguration 資料表](moduleconfiguration-table.md) 的 CoNtextData 資料行。</span><span class="sxs-lookup"><span data-stu-id="72d3e-109">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Bitfield is the value in the Format column.</span></span>
-   <span data-ttu-id="72d3e-110">當 Text 是 Format 資料行中的值，而 Enum 是 Type 資料行中的值時， [ModuleConfiguration 資料表](moduleconfiguration-table.md) 的 CoNtextData 資料行。</span><span class="sxs-lookup"><span data-stu-id="72d3e-110">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Text is the value in the Format column and Enum is the value in the Type column.</span></span>
-   <span data-ttu-id="72d3e-111">當索引鍵是 Format 資料行中的值時， [ModuleConfiguration 資料表](moduleconfiguration-table.md) 的 DefaultValue 資料行。</span><span class="sxs-lookup"><span data-stu-id="72d3e-111">The DefaultValue column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Key is the value in the Format column.</span></span>
-   <span data-ttu-id="72d3e-112">[**ProvideTextData 方法**](configuremodule-providetextdata.md)所使用之金鑰格式的可設定專案。</span><span class="sxs-lookup"><span data-stu-id="72d3e-112">Configurable items in the Key format used by the [**ProvideTextData method**](configuremodule-providetextdata.md).</span></span>

<span data-ttu-id="72d3e-113">若要以 CMSM 特殊格式輸入常值分號或等號字元，請在字元前面加上反斜線字元 ( ' \\ ' ) 。</span><span class="sxs-lookup"><span data-stu-id="72d3e-113">To enter literal semicolons or equal characters into a value in CMSM special format, prefix the character with a backslash character ('\\').</span></span> <span data-ttu-id="72d3e-114">常值反斜線可以用兩個反斜線表示。</span><span class="sxs-lookup"><span data-stu-id="72d3e-114">A literal backslash can be represented by two backslashes.</span></span> <span data-ttu-id="72d3e-115">前置詞為單一反斜線的單一字元會轉譯成單一字元，即使不需要將字元轉義也是一樣。</span><span class="sxs-lookup"><span data-stu-id="72d3e-115">A single character prefixed by a single backslash is translated into the single character, even if escaping the character is not required.</span></span>

<span data-ttu-id="72d3e-116">如果分號或等於字元沒有前置詞，但在值的內容中沒有定義的行為，則產生的字串會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="72d3e-116">If a semicolon or equals character is not prefixed by a backslash yet does not have a defined behavior in the context of the value, the resulting string is undefined.</span></span> <span data-ttu-id="72d3e-117">例如，ModuleConfiguration 資料表的 DefaultValue 資料行是所有索引鍵專案的 CMSM 特殊格式，因為分號字元是資料行分隔符號。</span><span class="sxs-lookup"><span data-stu-id="72d3e-117">For example, the DefaultValue column of the ModuleConfiguration table is in CMSM special format for all Key items because the semicolon character is the column delimiter.</span></span> <span data-ttu-id="72d3e-118">雖然在此字串中，等號字元沒有特殊意義，但常值相等的字元仍然必須在此字串中進行轉義。</span><span class="sxs-lookup"><span data-stu-id="72d3e-118">Although the equal character has no special meaning in this string, literal equal characters must still be escaped in this string.</span></span>

 

 



