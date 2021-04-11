---
description: ICE78 會確認 AdvtUISequence 資料表不存在或空白。 這是必要的，因為在廣告期間不允許任何使用者介面。
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113852"
---
# <a name="ice78"></a>ICE78

ICE78 會確認 [AdvtUISequence 資料表](advtuisequence-table.md) 不存在或空白。 這是必要的，因為在廣告期間不允許任何使用者介面。

## <a name="result"></a>結果

如果 AdvtUISequence 資料表存在且不是空的，ICE78 會張貼錯誤。

## <a name="example"></a>範例

ICE78 會報告此範例的下列錯誤：

在 AdvtUISequence 資料表中找到動作 ' Action1 '。 在廣告期間不允許任何使用者介面。 因此，AdvtUISequence 資料表必須是空的或不存在。

[AdvtUISequence 資料表](advtuisequence-table.md) (部分) 



| 動作  | 條件 | 順序 |
|---------|-----------|----------|
| Action1 | true      | 1        |



 

若要修正錯誤，請從資料表中移除 "Action1"，或移除資料表。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



