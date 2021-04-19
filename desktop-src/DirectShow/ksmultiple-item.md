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
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998633"
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

[DirectShow 結構](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




