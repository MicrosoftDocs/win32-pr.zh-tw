---
description: KSMULTIPLE \_ 專案結構描述核心模式 pin 上可變長度屬性的大小和計數。
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: 'KSMULTIPLE_ITEM 結構 (Ks) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 2e1cdf3d8edcea88fbcfb260d87d3e79d62eb2aebc57144ae38defb018065f1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823308"
---
# <a name="ksmultiple_item-structure"></a>KSMULTIPLE \_ 專案結構

`KSMULTIPLE_ITEM`結構描述核心模式 pin 上可變長度屬性的大小和計數。

## <a name="syntax"></a>語法


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a>成員

<dl> <dt>

**大小**
</dt> <dd>

傳回之記憶體區塊的大小（以位元組為單位）。 大小包含 **KSMULTIPLE \_ 專案** 結構和其後的專案。

</dd> <dt>

**Count**
</dt> <dd>

指定遵循此結構的總專案數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Ks. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow結構](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




