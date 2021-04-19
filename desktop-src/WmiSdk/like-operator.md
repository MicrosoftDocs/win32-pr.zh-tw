---
description: LIKE 運算子會判斷字元字串是否符合指定的模式。
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: LIKE 運算子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981516"
---
# <a name="like-operator"></a><span data-ttu-id="f7edd-103">LIKE 運算子</span><span class="sxs-lookup"><span data-stu-id="f7edd-103">LIKE Operator</span></span>

<span data-ttu-id="f7edd-104">LIKE 運算子會判斷字元字串是否符合指定的模式。</span><span class="sxs-lookup"><span data-stu-id="f7edd-104">The LIKE operator determines whether or not a character string matches a specified pattern.</span></span> <span data-ttu-id="f7edd-105">指定的模式可以剛好包含要比對的字元，或可包含中繼字元。</span><span class="sxs-lookup"><span data-stu-id="f7edd-105">The specified pattern can contain exactly the characters to match, or it can contain meta characters.</span></span> <span data-ttu-id="f7edd-106">實際上，LIKE 運算子會使用下表中的萬用字元來比對子字串。</span><span class="sxs-lookup"><span data-stu-id="f7edd-106">In effect, the LIKE operator matches substrings using the wildcard characters in the following table.</span></span>



| <span data-ttu-id="f7edd-107">字元</span><span class="sxs-lookup"><span data-stu-id="f7edd-107">Character</span></span>       | <span data-ttu-id="f7edd-108">描述</span><span class="sxs-lookup"><span data-stu-id="f7edd-108">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7edd-109">\[ \]</span><span class="sxs-lookup"><span data-stu-id="f7edd-109">\[ \]</span></span>           | <span data-ttu-id="f7edd-110">指定範圍內的任何一個字元 (\[ a-f \]) 或設定 (\[ abcdef \]) 。</span><span class="sxs-lookup"><span data-stu-id="f7edd-110">Any one character within the specified range (\[a-f\]) or set (\[abcdef\]).</span></span>                                                                                                                 |
| ^               | <span data-ttu-id="f7edd-111">不在範圍內的任何一個字元 (\[ ^ a-f \]) 或設定 (\[ ^ abcdef \] 。 ) </span><span class="sxs-lookup"><span data-stu-id="f7edd-111">Any one character not within the range (\[^a-f\]) or set (\[^abcdef\].)</span></span>                                                                                                                     |
| %               | <span data-ttu-id="f7edd-112">0 () 零或多個字元的任何字串。</span><span class="sxs-lookup"><span data-stu-id="f7edd-112">Any string of 0 (zero) or more characters.</span></span> <span data-ttu-id="f7edd-113">下列範例會尋找在類別名稱中任何位置都找到 "Win" 的所有實例： `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span><span class="sxs-lookup"><span data-stu-id="f7edd-113">The following example finds all instances where "Win" is found anywhere in the class name: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span></span> |
| <span data-ttu-id="f7edd-114">\_ (底線) </span><span class="sxs-lookup"><span data-stu-id="f7edd-114">\_ (underscore)</span></span> | <span data-ttu-id="f7edd-115">任何一個字元。</span><span class="sxs-lookup"><span data-stu-id="f7edd-115">Any one character.</span></span> <span data-ttu-id="f7edd-116">在查詢字串中使用的任何常值底線都必須透過將其放在 \[ \] (方括弧) 內進行轉義。</span><span class="sxs-lookup"><span data-stu-id="f7edd-116">Any literal underscore used in the query string must be escaped by placing it inside \[\] (square brackets).</span></span>                                                             |



 

<span data-ttu-id="f7edd-117">例如，下列 Power shell 程式碼會抓取 **名稱** 屬性以 **FirstName** 開頭的 **Win32 \_ 作業系統** 類別的所有實例：</span><span class="sxs-lookup"><span data-stu-id="f7edd-117">For example, the following Power shell code retrieves all instances of the **Win32\_operatingSystem** class whose **Name** property begins with **FirstName**:</span></span>

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

<span data-ttu-id="f7edd-118">因為底線是中繼字元，所以如果查詢目標有底線，則 " \[ \] " escape 字元必須括住。</span><span class="sxs-lookup"><span data-stu-id="f7edd-118">Because the underscore is a meta character, if the query target has an underscore, the "\[\]" escape characters must surround it.</span></span> <span data-ttu-id="f7edd-119">例如，您可以查詢名稱中有雙底線的所有類別。</span><span class="sxs-lookup"><span data-stu-id="f7edd-119">For example, you can query for all the classes that have a double underscore in the name.</span></span>

<span data-ttu-id="f7edd-120">若要在名稱中找出具有雙底線的所有類別，您必須使用 (方括弧) 來將這兩個底線進行 escape \[ \] ，例如：</span><span class="sxs-lookup"><span data-stu-id="f7edd-120">To locate all classes with a double underscore in the name, you must escape both underscores with \[\] (square brackets), for example:</span></span>

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

<span data-ttu-id="f7edd-121">您可以使用 NOT 來否定 LIKE 語句;若要這樣做，請務必將不直接放在功能變數名稱前面。</span><span class="sxs-lookup"><span data-stu-id="f7edd-121">You can negate a LIKE statement using NOT; to do so, be sure to place the NOT directly in front of the field name.</span></span> <span data-ttu-id="f7edd-122">例如：</span><span class="sxs-lookup"><span data-stu-id="f7edd-122">For example:</span></span>

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a><span data-ttu-id="f7edd-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7edd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7edd-124">WQL 運算子</span><span class="sxs-lookup"><span data-stu-id="f7edd-124">WQL Operators</span></span>](wql-operators.md)
</dt> </dl>

 

 



