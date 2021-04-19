---
title: 物件 (DN-字串) 語法
description: 包含字串值和 DN 的八位字串。
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- 物件 (DN-字串) 語法 AD 架構
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991315"
---
# <a name="objectdn-string-syntax"></a>物件 (DN-字串) 語法

包含字串值和 DN 的八位字串。



| 進入 | 值 |
|--------------|------------------------------------------------------------------------------------|
| 名稱         | Object(DN-String)                                                                  |
| 語法識別碼    | 2.5.5.14                                                                           |
| OM 識別碼        | 127                                                                                |
| MAPI 類型    | \-                                                                                 |
| ADS 類型     | \_ \_ 以字串 ADSTYPE \_ DN                                                          |
| Variant 類型 | VT \_ 分派                                                                       |
| SDS 類型     | 可以轉換成 [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)的 COM 物件。 |



## <a name="remarks"></a>備註

具有此語法的值具有下列格式：

``` syntax
S:<char count>:<string value>:<object DN>
```

其中「 &lt; char count」 &gt; 是「字串值」字串中的字元數 &lt; &gt; ，而「 &lt; 物件 DN」 &gt; 是 Active Directory 中物件的分辨名稱。 如果移動或重新命名它所參考的物件，Active Directory 會更新 DN。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
