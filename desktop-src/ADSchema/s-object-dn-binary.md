---
title: 物件 (DN-二進位) 語法
description: 包含二進位值的八位字串以及 (DN) 的分辨名稱。
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- 物件 (DN-二進位) 語法 AD 架構
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106703"
---
# <a name="objectdn-binary-syntax"></a>物件 (DN-二進位) 語法

包含二進位值的八位字串以及 (DN) 的分辨名稱。



| 進入 | 值 |
|--------------|------------------------------------------------------------------------------------|
| 名稱         | Object(DN-Binary)                                                                  |
| 語法識別碼    | 2.5.5.7                                                                            |
| OM 識別碼        | 127                                                                                |
| MAPI 類型    | TSTRING                                                                            |
| ADS 類型     | \_ \_ 使用二進位 ADSTYPE \_ DN                                                          |
| Variant 類型 | VT \_ 分派                                                                       |
| SDS 類型     | 可以轉換成 [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)的 COM 物件。 |



## <a name="remarks"></a>備註

具有此語法的值具有下列格式：

``` syntax
B:<char count>:<binary value>:<object DN>
```

其中「 &lt; char count」 &gt; 是「二進位值」中的十六進位數位數目 &lt; ，「 &gt; &lt; 二進位值」 &gt; 是二進位值的十六進位標記法，而「 &lt; 物件 DN」 &gt; 是辨別名稱。 如果移動或重新命名它所參考的物件，Active Directory 會自動更新該 DN。 如需使用此語法的詳細資訊和程式碼範例，請參閱 [使用 OtherWellKnownObjects 屬性啟用重新命名安全](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property)系結。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
