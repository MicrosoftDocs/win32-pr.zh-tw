---
description: PF \_ HANDOFFENTRY 結構會定義網路監視器新增至剖析器之遞交集的通訊協定。
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: 'PF_HANDOFFENTRY 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: faf98490424754d6ae2223ca063e0e3a4eec69c113b1a220e9657b7db5edbb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778668"
---
# <a name="pf_handoffentry-structure"></a>PF \_ HANDOFFENTRY 結構

**PF \_ HANDOFFENTRY** 結構會定義網路監視器新增至剖析器之遞交集的通訊協定。

## <a name="syntax"></a>語法


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**szIniFile**
</dt> <dd>

與通訊協定相關聯的 INI 檔案名。

</dd> <dt>

**szIniSection**
</dt> <dd>

INI 檔案中的區段標籤。

</dd> <dt>

**szProtocol**
</dt> <dd>

通訊協定的名稱。

</dd> <dt>

**dwHandOffValue**
</dt> <dd>

與通訊協定相關聯的值。

</dd> <dt>

**ValueFormatBase**
</dt> <dd>

**DwHandOffValue** 中指定之通訊協定值的數位基底。 **ValueFormatBase** 函數必須設定為下列其中一項：



| 值                                                                                                                                                                                                                        | 意義                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**提交 \_ 值 \_ 格式 \_ 基底 \_ 未知**</dt> </dl> | 未知的基底<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**切換 \_ 值 \_ 格式 \_ 基底 \_ 十進位**</dt> </dl> | 十進位基底<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**提交 \_ 值 \_ 格式 \_ 基底 \_ 十六進位**</dt> </dl>             | 十六進位基底<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

Pf [ \_ HANDOFFSET](pf-handoffset.md)結構中會使用 **pf \_ HANDOFFENTRY** 結構的陣列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> </dl>

 

 




