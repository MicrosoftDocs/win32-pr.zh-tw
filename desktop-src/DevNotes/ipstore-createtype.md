---
description: 使用指定的名稱建立指定的型別。
ms.assetid: eb85477c-d750-46d2-8b32-450f672e7601
title: 'IPStore：： CreateType 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7064cd07c0af99cbb325457217c2679757837be3ac1f5d80977cd2bb222f6b75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667516"
---
# <a name="ipstorecreatetype-method"></a>IPStore：： CreateType 方法

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

使用指定的名稱建立指定的型別。

## <a name="syntax"></a>語法


```C++
HRESULT CreateType(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO pInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

指定類型是否為本機電腦，或僅與建立的使用者相關聯。



| 值                                                                                                                                                                                                                                                   | 意義                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt> </dl>    | 存放區會保留在登錄的 [目前使用者] 區段中。<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt> </dl> | 存放區會保留在登錄的 [本機電腦] 區段中。<br/> |



 

</dd> <dt>

*pType* \[在\]
</dt> <dd>

識別儲存體資料類型之 **GUID** 的指標。

</dd> <dt>

*pInfo* \[在\]
</dt> <dd>

包含資料類型名稱之 [**PST \_ TYPEINFO**](pst-typeinfo.md) 結構的指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

Reserved：必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT** 值。 值為 **PST \_ E \_ OK** 表示函式已成功。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**PST \_ TYPEINFO**](pst-typeinfo.md)
</dt> </dl>

 

 
