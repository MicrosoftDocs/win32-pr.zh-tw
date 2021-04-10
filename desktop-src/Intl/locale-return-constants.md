---
description: 地區設定傳回 \_ \* 常數
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: LOCALE_RETURN * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194548"
---
# <a name="locale_return-constants"></a><span data-ttu-id="1f8c0-103">地區設定傳回 \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="1f8c0-103">LOCALE\_RETURN\* Constants</span></span>

<span data-ttu-id="1f8c0-104">本主題定義 NLS 所使用的地區設定傳回 \_ \* 常數。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-104">This topic defines the LOCALE\_RETURN\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f8c0-105">值</span><span class="sxs-lookup"><span data-stu-id="1f8c0-105">Value</span></span></th>
<th><span data-ttu-id="1f8c0-106">意義</span><span class="sxs-lookup"><span data-stu-id="1f8c0-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f8c0-107">LOCALE_RETURN_GENITIVE_NAMES</span><span class="sxs-lookup"><span data-stu-id="1f8c0-107">LOCALE_RETURN_GENITIVE_NAMES</span></span></td>
<td><span data-ttu-id="1f8c0-108"><strong>Windows 7 和更新版本：</strong> 取出月份的所有格名稱，這些名稱是月份名稱與其他專案合併時所使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-108"><strong>Windows 7 and later:</strong> Retrieve the genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="1f8c0-109">例如，在「烏克蘭」中， &quot; &quot; 當月份單獨命名時，會將相當於1月的Січень寫入。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-109">For example, in Ukrainian the equivalent of January is written &quot;Січень&quot; when the month is named alone.</span></span> <span data-ttu-id="1f8c0-110">不過，當月份名稱用於組合時（例如，在2003年1月5日的日期）中，會使用名稱的所有格形式。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-110">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="1f8c0-111">針對烏克蘭範例，所有格月份名稱會顯示為 &quot; 5 січня 2003 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-111">For the Ukrainian example, the genitive month name is displayed as &quot;5 січня 2003&quot;.</span></span> <span data-ttu-id="1f8c0-112">所有格月份名稱的清單會從1月開始，並以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-112">The list of genitive month names begins with January and is semicolon-delimited.</span></span> <span data-ttu-id="1f8c0-113">如果沒有13個月，請在清單結尾使用分號。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-113">If there is no 13th month, use a semicolon in its place at the end of the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f8c0-114">所有語言都不會有所有格的月份名稱。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-114">Genitive month names do not exist in all languages.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8c0-115">LOCALE_RETURN_NUMBER</span><span class="sxs-lookup"><span data-stu-id="1f8c0-115">LOCALE_RETURN_NUMBER</span></span></td>
<td><span data-ttu-id="1f8c0-116"><strong>Windows Me/98、Windows NT 4.0 和更新版本：</strong> 取出數位。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-116"><strong>Windows Me/98, Windows NT 4.0 and later:</strong> Retrieve a number.</span></span> <span data-ttu-id="1f8c0-117">這個常數會造成 <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> 或 <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> 以數位形式（而不是字串）來取出值。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-117">This constant causes <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> to retrieve a value as a number instead of as a string.</span></span> <span data-ttu-id="1f8c0-118">接收值的緩衝區必須至少為 DWORD 值的長度。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-118">The buffer that receives the value must be at least the length of a DWORD value.</span></span> <span data-ttu-id="1f8c0-119">這個常數可以與名稱開頭為 LOCALE_I 的任何其他常數合併 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="1f8c0-119">This constant can be combined with any other constant having a name that begins with &quot;LOCALE_I&quot;.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




