---
description: PATTERNMATCH 結構會定義用來評估框架的模式元素。
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: 'PATTERNMATCH 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944518"
---
# <a name="patternmatch-structure"></a>PATTERNMATCH 結構

**PATTERNMATCH** 結構會定義用來評估框架的模式元素。

## <a name="syntax"></a>語法


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a>成員

<dl> <dt>

**旗標**
</dt> <dd>

模式相符旗標：



| 值                                                                                                                                                                                                                                                                                           | 意義                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <dt>**模式 \_比對 \_ 旗標 \_ 不**</dt>是 <dt>0x00000001</dt> </dl>                                   | 設定時，此旗標會在適當的位置保留缺少指定模式的框架。<br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <dt>**模式 \_符合 \_ 旗標 \_ 埠 \_ 指定**</dt> <dt>0x00000008</dt> </dl> | 搜尋埠號碼值。<br/>                                                             |



 

</dd> <dt>

**OffsetBasis**
</dt> <dd>

Offset 的類型，可以是下列其中一項：



| 值                                                                                                                                                                                                                                                       | 意義                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <dt>**\_ \_ 相對 \_ 于框架的位移基準 \_**</dt> </dl>                                         | 設定相對於框架開頭的位移（以位元組為單位）。<br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <dt>**\_ \_ 相對 \_ 于 \_ 有效 \_ 通訊協定的位移**</dt> </dl> | 設定相對於參考之通訊協定開頭的位移（以位元組為單位）。<br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <dt>**\_ \_ 相對 \_ 于 IPX 的位移基礎 \_**</dt> </dl>                                               | 設定相對於 IPX 的位移（以位元組為單位）。<br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <dt>**\_ \_ 相對 \_ 于 IP 的位移基準 \_**</dt> </dl>                                                  | 設定相對於 IP 的位移（以位元組為單位）。<br/>                              |



 

</dd> <dt>

**通訊埠**
</dt> <dd>

埠值（如果有指定）。

</dd> <dt>

**Offset**
</dt> <dd>

相對於 **OffsetBasis** 的位移（以位元組為單位）。

</dd> <dt>

**長度**
</dt> <dd>

相符模式的長度。

</dd> <dt>

**PatternToMatch**
</dt> <dd>

要比對的模式。

</dd> </dl>

## <a name="remarks"></a>備註

此結構是用來建立 capture 篩選器。 如需有關如何執行此結構的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md)」。

捕獲篩選最多可包含四個 **PATTERNMATCH** 結構。

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

 

 




