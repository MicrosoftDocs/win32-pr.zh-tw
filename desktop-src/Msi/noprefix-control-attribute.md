---
description: 如果在文字控制項上設定此位，則文字字串中出現的字元 &\# 0034; &&\# 0034; 會顯示為本身。 如果未設定此位，則 \# 會將文字字串中的字元 &0034; &&\# 0034;）顯示為帶字元字元。
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191862"
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

 

 



