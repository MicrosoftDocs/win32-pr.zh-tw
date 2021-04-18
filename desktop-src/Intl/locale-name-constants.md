---
description: 地區設定 \_ 名稱 \* 常數
ms.assetid: 63e2e368-af2f-4af0-bbea-2b27d1939394
title: LOCALE_NAME * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aaaba8665c729a047be6a7e3a3d6b3239c81af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978041"
---
# <a name="locale_name-constants"></a><span data-ttu-id="d62c6-103">地區設定 \_ 名稱 \* 常數</span><span class="sxs-lookup"><span data-stu-id="d62c6-103">LOCALE\_NAME\* Constants</span></span>

<span data-ttu-id="d62c6-104">本主題定義 NLS 所使用的地區設定 \_ 名稱 \* 常數。</span><span class="sxs-lookup"><span data-stu-id="d62c6-104">This topic defines the LOCALE\_NAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d62c6-105">值</span><span class="sxs-lookup"><span data-stu-id="d62c6-105">Value</span></span></th>
<th><span data-ttu-id="d62c6-106">意義</span><span class="sxs-lookup"><span data-stu-id="d62c6-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d62c6-107">LOCALE_NAME_INVARIANT</span><span class="sxs-lookup"><span data-stu-id="d62c6-107">LOCALE_NAME_INVARIANT</span></span></td>
<td><span data-ttu-id="d62c6-108">提供穩定地區設定和行事歷數據的不變地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="d62c6-108">Name of an invariant locale that provides stable locale and calendar data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d62c6-109">LOCALE_NAME_MAX_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d62c6-109">LOCALE_NAME_MAX_LENGTH</span></span></td>
<td><span data-ttu-id="d62c6-110">地區設定名稱的最大長度。</span><span class="sxs-lookup"><span data-stu-id="d62c6-110">Maximum length of a locale name.</span></span> <span data-ttu-id="d62c6-111">此字串允許的最大字元數為85，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="d62c6-111">The maximum number of characters allowed for this string is 85, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d62c6-112">您的應用程式必須使用常數來取得最大的地區設定名稱長度，而不是對值85進行硬式編碼 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="d62c6-112">Your application must use the constant for the maximum locale name length, instead of hard-coding the value &quot;85&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d62c6-113">LOCALE_NAME_SYSTEM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d62c6-113">LOCALE_NAME_SYSTEM_DEFAULT</span></span></td>
<td><span data-ttu-id="d62c6-114">目前作業系統地區設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="d62c6-114">Name of the current operating system locale.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d62c6-115">LOCALE_NAME_USER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d62c6-115">LOCALE_NAME_USER_DEFAULT</span></span></td>
<td><span data-ttu-id="d62c6-116">目前使用者地區設定的名稱，符合主控台的 [地區及語言選項] 部分中的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="d62c6-116">Name of the current user locale, matching the preference set in the regional and language options portion of Control Panel.</span></span> <span data-ttu-id="d62c6-117">此地區設定可能與目前使用者介面語言的地區設定不同。</span><span class="sxs-lookup"><span data-stu-id="d62c6-117">This locale can be different from the locale for the current user interface language.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




