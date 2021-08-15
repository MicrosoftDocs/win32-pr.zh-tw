---
description: HANDOFFENTRY 結構會在 HANDOFFTABLE 結構中定義特定的通訊協定專案。
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: 'HANDOFFENTRY 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 692b9e925442920a67434f74c9e8a8ebd225fc417cbbf419b6eb568aa9eee2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981411"
---
# <a name="handoffentry-structure"></a>HANDOFFENTRY 結構

**HANDOFFENTRY** 結構會在 **HANDOFFTABLE** 結構中定義特定的通訊協定專案。

根據使用者在呼叫 [**CreateHandoffTable**](createhandofftable.md) 函式時提供的 .ini 檔案中提供的資訊，網路監視器填入此結構。 應用程式絕對不應明確修改此結構。

## <a name="syntax"></a>語法


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**hoe \_ sig**
</dt> <dd>

將此專案識別為遞交資料表專案的簽章。

</dd> <dt>

**hoe \_ ProtIdentNumber**
</dt> <dd>

使用者提供的 .ini 檔案所提供的通訊協定編號。

</dd> <dt>

**hoe \_ ProtocolHandle**
</dt> <dd>

使用使用者提供的 .ini 檔案所提供的通訊協定名稱所建立的通訊協定控制碼。

</dd> <dt>

**hoe \_ ProtocolData**
</dt> <dd>

使用者提供的通訊協定實例資料 .ini 檔。

</dd> </dl>

## <a name="remarks"></a>備註

當網路監視器建立遞交資料表時，網路監視器會填入此結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




