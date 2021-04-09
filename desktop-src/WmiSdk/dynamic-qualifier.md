---
description: 動態辨識符號表示以動態方式建立實例的類別。 此限定詞的值必須設定為 TRUE。
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: 動態限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848743"
---
# <a name="dynamic-qualifier"></a>動態限定詞

**動態** 辨識符號表示以動態方式建立實例的類別。 此限定詞的值必須設定為 **TRUE**。

您必須在所有包含資料的類別，以及動態建立的實例上指定 **動態** 限定詞。 通常也會指定 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號，以識別負責提供資料的提供者。

只包含需要執行之方法的類別不需要 **動態** 限定詞。 只有 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號需要指定提供者的名稱，才能提供執行。

所有衍生自動態類別的類別都必須是動態的。 您無法從動態類別衍生靜態類別。

當在實例的屬性上指定 **動態** 時，也必須指定 **PropertyCoNtext** 限定詞。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**標準 WMI 限定詞**](standard-wmi-qualifiers.md)
</dt> <dt>

[WMI 限定詞](wmi-qualifiers.md)
</dt> <dt>

[新增限定詞](adding-a-qualifier.md)
</dt> </dl>

 

 




