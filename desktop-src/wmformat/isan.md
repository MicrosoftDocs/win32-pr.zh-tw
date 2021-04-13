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
# <a name="isan"></a>ISAN

**ISAN** 屬性包含識別內容 (ISAN) 的國際標準視聽號碼。

## <a name="global-constant"></a>全域常數

g \_ wszISAN

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

ISAN 是識別視聽運作的國際標準。 如需 ISAN 的相關資訊，請造訪標準 [網站](https://www.isan.org/)。

當您設定這個屬性時，中繼資料編輯器物件會驗證 ISAN 字串。 可接受的字串格式（如 ISAN 規格的4.1 章節所述）包含16個十六進位數位，可選擇性地以空白字元或連字號分隔為4位數的區段。 格式化的數位必須依照有效的檢查字元，以空格或連字號分隔。 檢查字元可以是十進位數或大寫字母。 如需有關如何衍生檢查編號的詳細資訊，請參閱 ISAN 使用者指南的附錄 A。

標準 ISAN 字串後面可能接著版本資訊。 如果有的話，版本資訊包含八個十六進位數位，後面接著一個檢查編號。 這些字元的格式會遵循與基底字元串相同的規則。

## <a name="examples"></a>範例

以下是範例 ISAN 的三個可接受格式字串。


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



下列字串顯示具有版本資訊的 ISAN 格式。


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




