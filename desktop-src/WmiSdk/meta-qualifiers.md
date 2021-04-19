---
description: 中繼限定詞會藉由在 MOF 語法中明確地定義類別或屬性宣告的實際使用方式，來精簡 CIM 模型中中繼結構的定義。
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: 中繼限定詞
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984593"
---
# <a name="meta-qualifiers"></a>中繼限定詞

中繼限定詞會藉由在 MOF 語法中明確地定義類別或屬性宣告的實際使用方式，來精簡 CIM 模型中中繼結構的定義。

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**協會**
</dt> <dd>

資料類型： **布林值**

適用于：類別

指出類別是否為關聯類別，用來描述兩個其他類別之間的關聯性。 缺少這個辨識符號表示類別不是關聯類別。 此辨識符號與 **指示** 互斥。 如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**指示**
</dt> <dd>

資料類型： **布林值**

適用于：類別

指出物件類別是否會定義指示。 此辨識符號與 **關聯** 互斥。 預設值為 **FALSE**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 限定詞](wmi-qualifiers.md)
</dt> <dt>

[新增限定詞](adding-a-qualifier.md)
</dt> </dl>

 

 




