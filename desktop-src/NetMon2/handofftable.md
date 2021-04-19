---
description: HANDOFFTABLE 結構會定義出交付資料表的通訊協定。
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: 'HANDOFFTABLE 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991685"
---
# <a name="handofftable-structure"></a>HANDOFFTABLE 結構

**HANDOFFTABLE** 結構會定義出交付資料表的通訊協定。

根據使用者在呼叫 [**CreateHandoffTable**](createhandofftable.md) 函式時提供的 .ini 檔中的資訊，網路監視器填入此結構。

## <a name="syntax"></a>語法


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**熱 \_ sig**
</dt> <dd>

將此資料表識別為遞交資料表的簽章。

</dd> <dt>

**熱 \_ NumEntries**
</dt> <dd>

網路監視器加入至遞交資料表的專案數目。

</dd> <dt>

**熱門 \_ 專案**
</dt> <dd>

提交資料表。

</dd> </dl>

## <a name="remarks"></a>備註

當網路監視器建立一個遞交資料表時，網路監視器會填入此結構及其相關聯的 HANDOFFENTRY 結構。

當呼叫 [**CreateHandoffTable**](createhandofftable.md) 時，會在應用程式提供的 .ini 檔案中提供建立遞交資料表時所使用的通訊協定資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[HANDOFFENTRY](handoffentry.md)
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> </dl>

 

 




