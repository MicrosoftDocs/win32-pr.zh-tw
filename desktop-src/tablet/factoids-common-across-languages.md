---
description: 許多 factoids 描述所有語言辨識器通用的輸入，且不需要針對不同的語言使用不同的格式。 下表列出所有語言之間的通用 factoids。
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: 跨語言的通用 Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971235"
---
# <a name="factoids-common-across-languages"></a><span data-ttu-id="b2df9-104">跨語言的通用 Factoids</span><span class="sxs-lookup"><span data-stu-id="b2df9-104">Factoids Common Across Languages</span></span>

<span data-ttu-id="b2df9-105">許多 factoids 描述所有語言辨識器通用的輸入，且不需要針對不同的語言使用不同的格式。</span><span class="sxs-lookup"><span data-stu-id="b2df9-105">A number of factoids describe input that is common to all language recognizers and need not have different formats for different languages.</span></span> <span data-ttu-id="b2df9-106">下表列出所有語言之間的通用 factoids。</span><span class="sxs-lookup"><span data-stu-id="b2df9-106">The following table lists factoids that are common across all languages.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2df9-107">標記</span><span class="sxs-lookup"><span data-stu-id="b2df9-107">Factoid</span></span></th>
<th><span data-ttu-id="b2df9-108">定義</span><span class="sxs-lookup"><span data-stu-id="b2df9-108">Definition</span></span></th>
<th><span data-ttu-id="b2df9-109">範例</span><span class="sxs-lookup"><span data-stu-id="b2df9-109">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2df9-110"><strong>數位</strong></span><span class="sxs-lookup"><span data-stu-id="b2df9-110"><strong>Digit</strong></span></span></td>
<td><span data-ttu-id="b2df9-111">設定單一數位的偏差。</span><span class="sxs-lookup"><span data-stu-id="b2df9-111">Sets bias for a single digit.</span></span> <span data-ttu-id="b2df9-112">辨識器在設定此模擬項時，會偏向只傳回單一位數。</span><span class="sxs-lookup"><span data-stu-id="b2df9-112">The recognizer is biased toward returning only single digits when this factoid is set.</span></span><br/></td>
<td><span data-ttu-id="b2df9-113">0-9</span><span class="sxs-lookup"><span data-stu-id="b2df9-113">0-9</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2df9-114"><strong>電子郵件</strong></span><span class="sxs-lookup"><span data-stu-id="b2df9-114"><strong>Email</strong></span></span></td>
<td><span data-ttu-id="b2df9-115">設定電子郵件地址的偏差。</span><span class="sxs-lookup"><span data-stu-id="b2df9-115">Sets bias for an email address.</span></span><br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2df9-116"><strong>Web</strong></span><span class="sxs-lookup"><span data-stu-id="b2df9-116"><strong>Web</strong></span></span></td>
<td><span data-ttu-id="b2df9-117">設定各種 URL 格式的偏差。</span><span class="sxs-lookup"><span data-stu-id="b2df9-117">Sets bias for various URL formats.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b2df9-118">辨識器的預設設定包括 <strong>Web</strong> 模擬程式。</span><span class="sxs-lookup"><span data-stu-id="b2df9-118">The default settings for the recognizer include the <strong>Web</strong> factoid.</span></span> <span data-ttu-id="b2df9-119">因此，您可能不會注意到 <strong>Web</strong> 模擬程式和預設設定之間有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="b2df9-119">Because of this, you may not notice a large difference between the <strong>Web</strong> factoid and the default setting.</span></span> <span data-ttu-id="b2df9-120">不過， <strong>網路</strong> 模擬可協助消除 URL 中的單字之間的空格。</span><span class="sxs-lookup"><span data-stu-id="b2df9-120">However, the <strong>Web</strong> factoid does help eliminate spaces between words in a URL.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="b2df9-121">HTTP： \\ microsoft.net</span><span class="sxs-lookup"><span data-stu-id="b2df9-121">http:\\microsoft.net</span></span><br/> https://microsoft.us/<br/> <span data-ttu-id="b2df9-122">HTTPs： \\ www.microsoft.au </span><span class="sxs-lookup"><span data-stu-id="b2df9-122">https:\\www.microsoft.au</span></span>\<br/> https://microsoft.com<br/> <span data-ttu-id="b2df9-123">www.microsoft_world .com</span><span class="sxs-lookup"><span data-stu-id="b2df9-123">www.microsoft_world.com</span></span><br/> <span data-ttu-id="b2df9-124">www.microsoft.us </span><span class="sxs-lookup"><span data-stu-id="b2df9-124">www.microsoft.us</span></span>\<br/> <span data-ttu-id="b2df9-125">HTTP： \\www.microsoft.com\myfile.htm</span><span class="sxs-lookup"><span data-stu-id="b2df9-125">http:\\www.microsoft.com\myfile.htm</span></span><br/> <span data-ttu-id="b2df9-126">HTTP： \\www.microsoft.com\myfile.html</span><span class="sxs-lookup"><span data-stu-id="b2df9-126">http:\\www.microsoft.com\myfile.html</span></span><br/> <span data-ttu-id="b2df9-127">HTTP： \\ www. com\myfile.asp</span><span class="sxs-lookup"><span data-stu-id="b2df9-127">http:\\www.microsoft.com\myfile.asp</span></span><br/> <span data-ttu-id="b2df9-128">HTTP： \\ www.microsoft.uk</span><span class="sxs-lookup"><span data-stu-id="b2df9-128">http:\\www.microsoft.uk</span></span><br/> <span data-ttu-id="b2df9-129">HTTP： \\ www.microsoft.info</span><span class="sxs-lookup"><span data-stu-id="b2df9-129">http:\\www.microsoft.info</span></span><br/> <span data-ttu-id="b2df9-130">www.microsoft.biz</span><span class="sxs-lookup"><span data-stu-id="b2df9-130">www.microsoft.biz</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2df9-131"><strong>預設值</strong></span><span class="sxs-lookup"><span data-stu-id="b2df9-131"><strong>Default</strong></span></span></td>
<td><span data-ttu-id="b2df9-132">將辨識器傳回到其預設設定。</span><span class="sxs-lookup"><span data-stu-id="b2df9-132">Returns the recognizer to its default settings.</span></span><br/></td>
<td><span data-ttu-id="b2df9-133">西方語言的 factoids 預設設定包括系統字典、使用者字典、各種標點符號，以及 <strong>Web</strong> 和 <strong>數位</strong> factoids。</span><span class="sxs-lookup"><span data-stu-id="b2df9-133">The default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the <strong>Web</strong> and <strong>Number</strong> factoids.</span></span><br/> <span data-ttu-id="b2df9-134">東亞語言的 factoids 預設設定包含辨識器支援的所有字元。</span><span class="sxs-lookup"><span data-stu-id="b2df9-134">The default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2df9-135"><strong>None</strong></span><span class="sxs-lookup"><span data-stu-id="b2df9-135"><strong>None</strong></span></span></td>
<td><span data-ttu-id="b2df9-136">停用所有 factoids、字典和語言模型。</span><span class="sxs-lookup"><span data-stu-id="b2df9-136">Disables all factoids, dictionaries, and the language model.</span></span><br/></td>
<td><span data-ttu-id="b2df9-137">只有當您不希望辨識器使用任何文法規則或字典（包括系統字典）時，才應該使用此模擬。</span><span class="sxs-lookup"><span data-stu-id="b2df9-137">This factoid should be used only when you do not want the recognizer to use any grammar rules or dictionaries, including the system dictionary.</span></span> <span data-ttu-id="b2df9-138">這項模擬適用于輸入隨機字串，例如產品代碼。</span><span class="sxs-lookup"><span data-stu-id="b2df9-138">This factoid is useful for input of random strings such as product codes.</span></span> <span data-ttu-id="b2df9-139">請勿搭配此模擬使用強制旗標。</span><span class="sxs-lookup"><span data-stu-id="b2df9-139">Do not use the Coerce flag with this factoid.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




