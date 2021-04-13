---
title: ISAN
description: ISAN 屬性包含識別內容 (ISAN) 的國際標準視聽號碼。
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- ISAN windows Media 格式
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374638"
---
# <a name="isan"></a><span data-ttu-id="51a83-104">ISAN</span><span class="sxs-lookup"><span data-stu-id="51a83-104">ISAN</span></span>

<span data-ttu-id="51a83-105">**ISAN** 屬性包含識別內容 (ISAN) 的國際標準視聽號碼。</span><span class="sxs-lookup"><span data-stu-id="51a83-105">The **ISAN** attribute contains the International Standard Audiovisual Number (ISAN) that identifies the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="51a83-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="51a83-106">Global Constant</span></span>

<span data-ttu-id="51a83-107">g \_ wszISAN</span><span class="sxs-lookup"><span data-stu-id="51a83-107">g\_wszISAN</span></span>

## <a name="data-type"></a><span data-ttu-id="51a83-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="51a83-108">Data Type</span></span>

<span data-ttu-id="51a83-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="51a83-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="51a83-110">備註</span><span class="sxs-lookup"><span data-stu-id="51a83-110">Remarks</span></span>

<span data-ttu-id="51a83-111">ISAN 是識別視聽運作的國際標準。</span><span class="sxs-lookup"><span data-stu-id="51a83-111">ISAN is an international standard for identifying audiovisual works.</span></span> <span data-ttu-id="51a83-112">如需 ISAN 的相關資訊，請造訪標準 [網站](https://www.isan.org/)。</span><span class="sxs-lookup"><span data-stu-id="51a83-112">For information about ISAN, visit the standard's [Web site](https://www.isan.org/).</span></span>

<span data-ttu-id="51a83-113">當您設定這個屬性時，中繼資料編輯器物件會驗證 ISAN 字串。</span><span class="sxs-lookup"><span data-stu-id="51a83-113">The metadata editor object verifies the ISAN string when you set this attribute.</span></span> <span data-ttu-id="51a83-114">可接受的字串格式（如 ISAN 規格的4.1 章節所述）包含16個十六進位數位，可選擇性地以空白字元或連字號分隔為4位數的區段。</span><span class="sxs-lookup"><span data-stu-id="51a83-114">The acceptable string formatting, as described in section 4.1 of the ISAN specification, consists of 16 hexadecimal digits, optionally separated by whitespace or hyphens into 4-digit segments.</span></span> <span data-ttu-id="51a83-115">格式化的數位必須依照有效的檢查字元，以空格或連字號分隔。</span><span class="sxs-lookup"><span data-stu-id="51a83-115">The formatted number must be followed, also optionally separated by a space or hyphen, by a valid check character.</span></span> <span data-ttu-id="51a83-116">檢查字元可以是十進位數或大寫字母。</span><span class="sxs-lookup"><span data-stu-id="51a83-116">The check character can be a decimal digit or a capital letter.</span></span> <span data-ttu-id="51a83-117">如需有關如何衍生檢查編號的詳細資訊，請參閱 ISAN 使用者指南的附錄 A。</span><span class="sxs-lookup"><span data-stu-id="51a83-117">Refer to annex A of the ISAN user guide for information about how to derive the check number.</span></span>

<span data-ttu-id="51a83-118">標準 ISAN 字串後面可能接著版本資訊。</span><span class="sxs-lookup"><span data-stu-id="51a83-118">The standard ISAN string may be followed by version information.</span></span> <span data-ttu-id="51a83-119">如果有的話，版本資訊包含八個十六進位數位，後面接著一個檢查編號。</span><span class="sxs-lookup"><span data-stu-id="51a83-119">If present, version information consists of eight hexadecimal digits followed by a check number.</span></span> <span data-ttu-id="51a83-120">這些字元的格式會遵循與基底字元串相同的規則。</span><span class="sxs-lookup"><span data-stu-id="51a83-120">The formatting of these characters follows the same rules as the basic string.</span></span>

## <a name="examples"></a><span data-ttu-id="51a83-121">範例</span><span class="sxs-lookup"><span data-stu-id="51a83-121">Examples</span></span>

<span data-ttu-id="51a83-122">以下是範例 ISAN 的三個可接受格式字串。</span><span class="sxs-lookup"><span data-stu-id="51a83-122">The following are three acceptably formatted strings for an example ISAN.</span></span>


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



<span data-ttu-id="51a83-123">下列字串顯示具有版本資訊的 ISAN 格式。</span><span class="sxs-lookup"><span data-stu-id="51a83-123">The following string shows the format of an ISAN with version information.</span></span>


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a><span data-ttu-id="51a83-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51a83-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51a83-125">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="51a83-125">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




