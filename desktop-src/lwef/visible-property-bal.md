---
title: 'Visible 屬性 (Balloon 物件) '
description: 瞭解氣球物件的 Visible 屬性，它會針對指定的字元傳回或設定文字氣球的可見設定。
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101d454f90e01ebcf31619b935d1b90512648baf33a11883b6b971c3178fb871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975478"
---
# <a name="visible-property-balloon-object"></a>Visible 屬性 (Balloon 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

針對指定的字元，傳回或設定文字批註的可見設定。

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法** 
</dt> <dd>

*代理程式 ***。 (**"* CharacterID *" * * 的字元 ) 。球形提示。可見的* *  \[  =  *布林值*\]



| 部分      | 描述                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 布林運算式，指定是否顯示文字提示。<br/> **True** 氣球是可見的。<br/> **False** 這個氣球是隱藏的。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果您遵循 [**說**](speak-method.md)出或使用語句來嘗試變更氣球的屬性，它可能不會影響氣球的可見狀態，因為 **說** 出或 **思考** 呼叫會排入佇列，但呼叫設定球的可見狀態則不 [**會這麼做**](think-method.md)。 因此，只有在字元的佇列中沒有 **說話** 或 **思考** 電話時，才會設定此值。

如果您嘗試在字元是說話、移動或拖曳時設定這個屬性，則在先前的作業完成之前，屬性設定不會生效。

呼叫「 [**說話**](speak-method.md) 」和「 [**想法**](think-method.md) 」方法會自動使球顯示，將 [**visible**](visible-property.md) 屬性設為 **True**。 如果已啟用字元的 [自動隱藏隱藏] 屬性，則會在讀出輸出文字之後，自動隱藏球。 按一下或拖曳目前未說話的字元也會自動隱藏球標，即使停用自動隱藏設定也是如此。 您可以使用氣球的 [**Style**](style-property.md) 屬性來變更字元的 [自動隱藏] 設定。

### <a name="see-also"></a>另請參閱

[**Style 屬性**](style-property.md)


 

 





