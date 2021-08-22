---
description: 將字串和額外的資料加入至資料表。
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: pSetupStringTableAddStringEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 69aef5b206bec609aefd66b33bfa838471b944292767642aeef28f734c9c47b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386418"
---
# <a name="psetupstringtableaddstringex-function"></a>pSetupStringTableAddStringEx 函式

\[Windows Vista 或 Windows Server 2008 中無法使用此功能。\]

將字串和額外的資料加入至資料表。

## <a name="syntax"></a>語法


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StringTable* \[在\]
</dt> <dd>

字串資料表的指標。

</dd> <dt>

*字串* \[在\]
</dt> <dd>

要加入至資料表的字串指標。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

此參數的值可以是 `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` 。



| 值                                                                                                                                                                                                                                             | 意義                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <dt>**STRTAB \_區分 \_ 大小寫**</dt> <dt>0x001</dt> </dl> | 字串會區分大小寫。<br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <dt>**STRTAB \_新增 \_ EXTRADATA**</dt> <dt>0x004</dt> </dl>    | 有額外的資料。<br/>      |



 

</dd> <dt>

*ExtraData* \[在中，選擇性\]
</dt> <dd>

額外資料物件的選擇性指標。

</dd> <dt>

*ExtraDataSize* \[在中，選擇性\]
</dt> <dd>

額外資料的大小。

</dd> </dl>

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
