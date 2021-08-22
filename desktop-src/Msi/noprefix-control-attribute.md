---
description: 如果在文字控制項上設定此位，則文字字串中出現的字元 &\# 0034; &&\# 0034; 會顯示為本身。 如果未設定此位，則 \# 會將文字字串中的字元 &0034; &&\# 0034;）顯示為帶字元字元。
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15345bb56ad85ec654cffe7a0bf2173973e032ac33aca633105d3a220647cf93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065878"
---
# <a name="noprefix-control-attribute"></a>NoPrefix 控制項屬性

如果在文字控制項上設定此位，則文字字串中出現的字元 "&" 會顯示為本身。 如果未設定此位，則會將文字字串中 "&" 後面的字元顯示為帶底線。

## <a name="valid-controls"></a>有效的控制項

[Text](text-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                           |
|---------|-------------|------------------------------------|
| 131072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 NoPrefix 位。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



