---
description: ADDRESSTABLE 結構包含位址配對的表格。
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: 'ADDRESSTABLE 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c1c766e29033136954abab69755e1231e610983314cdaa01da3957889af5eb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064278"
---
# <a name="addresstable-structure"></a>ADDRESSTABLE 結構

**ADDRESSTABLE** 結構包含位址配對的表格。

## <a name="syntax"></a>語法


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**nAddressPairs**
</dt> <dd>

**AddressPair** 陣列中的位址組數目。

</dd> <dt>

**nNonMacAddressPairs**
</dt> <dd>

非 MAC 位址組的數目。

</dd> <dt>

**AddressPair**
</dt> <dd>

位址組的陣列。 請注意，您最多隻能為每個 ADDRESSTABLE 結構儲存八個位址組。

</dd> </dl>

## <a name="remarks"></a>備註

使用此結構作為 capture 篩選器結構處理的一部分。 如需有關如何執行此結構的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md)」。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




