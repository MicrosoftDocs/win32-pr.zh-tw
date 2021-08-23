---
description: 將資料項目寫入受保護的儲存體。
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'IPStore：： WriteItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d8af896d2aca8ae218ba06f94cb0e2ef5f86fc4122acf3463356f5fea3dafd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955887"
---
# <a name="ipstorewriteitem-method"></a>IPStore：： WriteItem 方法

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

將資料項目寫入受保護的儲存體。

## <a name="syntax"></a>語法


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

提供者存放區。



| 值                                                                                                                                                                                                                                                   | 意義                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt> </dl>    | 存放區會保留在登錄的 [目前使用者] 區段中。<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt> </dl> | 存放區會保留在登錄的 [本機電腦] 區段中。<br/> |



 

</dd> <dt>

*pItemType* \[在\]
</dt> <dd>

**GUID** 的指標，識別所寫入之資料項目的資料類型。

</dd> <dt>

*pItemSubtype* \[在\]
</dt> <dd>

**GUID** 的指標，識別所寫入之資料項目的資料子類型。

</dd> <dt>

*szItemName* \[在\]
</dt> <dd>

字串的指標，其中包含指派給預存資料項目的名稱。

</dd> <dt>

*cbData* \[擴展\]
</dt> <dd>

**DWORD** 的指標，指出包含儲存資料項目的緩衝區大小。

</dd> <dt>

*ppbData* \[擴展\]
</dt> <dd>

包含正在寫入之資料項目的緩衝區指標。

</dd> <dt>

*pProomptInfo* \[在\]
</dt> <dd>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)結構的指標。

</dd> <dt>

*dwDefaultConfirmationStyle* \[在\]
</dt> <dd>

預設確認樣式。



| 值                                                                                                                                                                                                                             | 意義                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**PST \_CF \_ 預設**</dt> <dt>0x00000000</dt> </dl> | 允許使用者選擇確認樣式。 <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**PST \_CF \_ 無**</dt> <dt>0x00000001</dt> </dl>          | 強制建立無訊息專案。 <br/>                      |



 

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

寫入操作的使用者介面和安全性行為。



| 值                                                                                                                                                                                                                                                              | 意義                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**PST \_無 \_ 覆寫**</dt> <dt>0x00000002</dt> </dl>                            | 指定要在受保護的儲存體中建立專案。 不允許覆寫現有的專案。<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_不受限制的 \_ ITEMDATA**</dt> <dt>0x00000004</dt> </dl> | 指定資料流程並非安全的。 依預設，專案呼叫是安全的。<br/>                         |



 

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

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
