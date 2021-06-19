---
title: 'Visible 屬性 (字元物件) '
description: 深入瞭解字元物件的 Visible 屬性，它會傳回布林值，指出是否可以看見該字元。
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396303"
---
# <a name="visible-property-characters-object"></a>Visible 屬性 (字元物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回布林值，指出字元是否可見。

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法** 
</dt> <dd>

*代理程式 ***。 (**"* CharacterID *" * * 的字元 ) 。可見**



| 值 | 描述                            |
|-------|----------------------------------------|
| True  | 字元隨即顯示。            |
| False | 隱藏的字元 (看不到) 。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性會指出是否顯示字元的畫面格。 這並不一定表示螢幕上有影像。 例如，即使字元位於可見的顯示區域或目前的字元框架未包含影像時，這個屬性也會傳回 **True** 。 這個屬性的設定會套用到字元的所有用戶端。

這是唯讀的屬性。 若要讓字元變成可見或隱藏，請使用 [**顯示**](show-method.md) 或 [**隱藏**](https://www.bing.com/search?q=**Hide**) 方法。

 

 




