---
title: 物件 (DS-DN) 語法
description: 包含辨別名稱 (DN) 的字串。
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- 物件 (DS-DN) 語法 AD 架構
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c9adf4138de56d90ac89743c3b428a1f25b45027bc19f0b5dccc2e005b143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835681"
---
# <a name="objectds-dn-syntax"></a>物件 (DS-DN) 語法

包含辨別名稱 (DN) 的字串。 若為具有此語法的屬性，Active Directory 會將屬性值處理為 DN 所識別之物件的參考，並在物件移動或重新命名時自動更新該值。 針對在篩選中包含 DN 語法屬性的查詢，請指定完整的分辨名稱。 萬用字元 (例如，cn = John \*) 不受支援。



| 進入 | 值 |
|--------------|------------------------------------------------------------------------|
| 名稱         | Object(DS-DN)                                                          |
| 語法識別碼    | 2.5.5.1                                                                |
| OM 識別碼        | 127                                                                    |
| MAPI 類型    | OBJECT                                                                 |
| ADS 類型     | ADSTYPE \_ DN \_ 字串                                                    |
| Variant 類型 | VT \_ BSTR                                                               |
| SDS 類型     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
