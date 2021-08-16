---
description: 從受保護的儲存體讀取指定的資料項目。
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'IPStore：： ReadItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 516eb55772e375d09d3b134dee456c090cf11d6ef0d10905f99a822b1df0d9e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001487"
---
# <a name="ipstorereaditem-method"></a>IPStore：： ReadItem 方法

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

從受保護的儲存體讀取指定的資料項目。

## <a name="syntax"></a>語法


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
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

GUID 的指標，識別要讀取之專案的資料類型。

</dd> <dt>

*pItemSubtype* \[在\]
</dt> <dd>

GUID 的指標，識別要讀取之專案的資料子類型。

</dd> <dt>

*szItemName* \[在\]
</dt> <dd>

字串的指標，其中包含指派給預存資料項目的名稱。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

**DWORD** ，指出包含儲存資料項目的緩衝區大小。

</dd> <dt>

*>pbdata* \[在\]
</dt> <dd>

包含儲存資料項目之緩衝區的指標。

</dd> <dt>

*pPromptInfo* \[在\]
</dt> <dd>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)結構的指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定讀取操作的使用者介面和安全性行為。

旗標值可以與邏輯 OR 合併。



| 值                                                                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_不受限制的 \_ ITEMDATA**</dt> <dt>0x00000004</dt> </dl> | 指定資料流程並非安全的。 依預設，專案呼叫是安全的。<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**PST \_提示 \_ 查詢**</dt> <dt>0x00000008</dt> </dl>                            | 指定在成功時傳回確認。 如果已啟用使用者介面，則會傳回 **PST \_ E \_ OK** 的成功。 如果未啟用使用者介面，則會傳回有 **PST \_ E \_ 專案 \_** 的值。<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_沒有任何 \_ UI \_ 遷移**</dt> <dt>0x00000010</dt> </dl>                  | 除非需要自訂密碼，否則不顯示使用者介面。<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT** 值。 值為 **PST \_ E \_ OK** 表示函式已成功。

## <a name="remarks"></a>備註

如果 **ReadItem** 順利完成，應用程式會負責使用 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函數釋放傳回的資料緩衝區。

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

 

 
