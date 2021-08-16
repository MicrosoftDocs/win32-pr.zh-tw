---
description: PROVIDOR \_ INFO \_ 2 結構會將列印提供者附加至列印提供者順序清單。
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: 'PROVIDOR_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 969af36fe0a64bb586fbf62912ca27c6ebba9ba0a627701e4bc57f6202bfe1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091678"
---
# <a name="providor_info_2-structure"></a>PROVIDOR \_ INFO \_ 2 結構

**PROVIDOR \_ INFO \_ 2** 結構會將列印提供者附加至列印提供者順序清單。

## <a name="syntax"></a>語法


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>成員

<dl> <dt>

**pOrder**
</dt> <dd>

以 null 結束的字串指標，指定列印提供者的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

呼叫 [**AddPrintProvidor**](addprintprovidor.md)（層級2）時，會使用這個結構，將指定的列印提供者加入至列印提供者順序清單的結尾。 如果呼叫成功，則會立即將提供者用於路由。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ PROVIDOR \_ Info \_ 2w** (Unicode) 和 **\_ PROVIDOR \_ INFO \_ 2a** (ANSI) <br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




