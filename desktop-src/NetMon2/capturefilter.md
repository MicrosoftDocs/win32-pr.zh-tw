---
description: CAPTUREFILTER 結構包含 capture 篩選資料。
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: 'CAPTUREFILTER 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983710"
---
# <a name="capturefilter-structure"></a>CAPTUREFILTER 結構

**CAPTUREFILTER** 結構包含 capture 篩選資料。

## <a name="syntax"></a>語法


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a>成員

<dl> <dt>

**FilterFlags**
</dt> <dd>

描述 capture 篩選器內容的旗標。



| 值                                                                                                                                                                                                                                                                                                   | 意義                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**CAPTUREFILTER \_旗標 \_ 包括 \_ 所有 \_ sap**</dt> <dt>0x0001</dt> </dl>       | 包含所有 Sap 作為可接受的框架。<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**CAPTUREFILTER \_旗標 \_ 包含 \_ 所有 \_ ETYPES**</dt> <dt>0x0002</dt> </dl> | 將所有 Etypes 包含為可接受的框架。<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**CAPTUREFILTER \_旗 \_ 標 \_ 僅限本機**</dt> <dt>0x0008</dt> </dl>                          | 無 P 模式<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**CAPTUREFILTER \_旗標 \_ 保留 \_ 原始**</dt> <dt>0x0020</dt> </dl>                                | 保留 SMT 和權杖環形 MAC 框架。<br/>      |



 

</dd> <dt>

**lpSapTable**
</dt> <dd>

SAP 值陣列的指標。 此成員會指出傳遞至驅動程式的有效 SAP 值。 如果 \_ 已設定 CAPTUREFILTER 旗標 \_ 包括 \_ 所有 \_ sap，則會變成例外狀況清單， (包含這些) 以外的所有 sap。

</dd> <dt>

**lpEtypeTable**
</dt> <dd>

Etype 值陣列的指標。 這會指出傳遞給驅動程式的這些 Etype 值都是有效的。 如果 \_ 已設定 CAPTUREFILTER 旗標，則會 \_ \_ \_ 變成例外清單， (包含這些) 以外的所有 ETYPES。

</dd> <dt>

**nSaps**
</dt> <dd>

SAP 資料表中的 sap 數目。

</dd> <dt>

**nEtypes**
</dt> <dd>

Etype 資料表中的 Etypes 數目。

</dd> <dt>

**AddressTable**
</dt> <dd>

位址資料表的名稱。

</dd> <dt>

**FilterExpression**
</dt> <dd>

運算式結構。 這包含 capture 篩選器的模式比對部分。

</dd> <dt>

**觸發程序**
</dt> <dd>

保留的。

</dd> <dt>

**nFrameBytesToCopy**
</dt> <dd>

如果此成員不是0，則會指定要保留每個框架的位元組數目。 如果是0，則保留整個框架。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> </dl>

## <a name="remarks"></a>備註

旗標、值和運算式的組合，會決定使用此結構資料的驅動程式將會傳遞哪些框架。 如需有關如何執行 **CAPTUREFILTER** 結構的詳細資訊，請參閱 [Capture 篩選器](capture-filters.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ADDRESSTABLE](addresstable.md)
</dt> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[表達](expression.md)
</dt> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




