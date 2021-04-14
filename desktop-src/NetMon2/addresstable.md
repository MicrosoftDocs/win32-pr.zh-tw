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
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469288"
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

 

 




