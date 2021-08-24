---
description: ADDRESSPAIR 結構會建立 capture 篩選器。
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: 'ADDRESSPAIR 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bbfc455951e76548694415434e0ee4b53893d594b8f0f31419e516bc466ed2c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744851"
---
# <a name="addresspair-structure"></a>ADDRESSPAIR 結構

**ADDRESSPAIR** 結構會建立 capture 篩選器。

## <a name="syntax"></a>語法


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a>成員

<dl> <dt>

**AddressFlags**
</dt> <dd>

描述捕獲篩選器所使用之位址的旗標。 如需詳細資訊，請參閱「備註」。



| 值                                                                                                                                                                                                         | 意義                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**位址 \_ 旗標 \_ 符合 \_ DST**</dt> </dl>                 | 符合目的地位址。<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**位址 \_ 旗標 \_ 符合 \_ SRC**</dt> </dl>                 | 符合來源位址。<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**排除的位址 \_ 旗標 \_**</dt> </dl>                     | 如果找到此位址，則排除框架。<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**位址 \_ 旗標 \_ DST \_ 群組 \_ 位址**</dt> </dl> | 僅符合群組位。 將此用於廣播類型的訊息。<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**\_ \_ 符合兩者的位址旗標 \_**</dt> </dl>              | 符合目的地和來源位址。<br/>                     |



 

</dd> <dt>

**NalReserved**
</dt> <dd>

這是保留的。

</dd> <dt>

**DstAddress**
</dt> <dd>

位址配對元素的目的地位址。

</dd> <dt>

**SrcAddress**
</dt> <dd>

位址配對元素的來源位址。

</dd> </dl>

## <a name="remarks"></a>備註

您可以結合 **AddressFlags** 成員的旗標。 例如，下列設定會在偵測到指定的來源位址時排除框架。

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

如需有關如何執行此結構的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md)」。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




