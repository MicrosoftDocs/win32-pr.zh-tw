---
description: 從受保護的儲存體中刪除指定的專案。
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: 'IPStore：:D eleteItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e99a2ec9b39b035b4a4af24aa18c2936decd399043cc507ed0bf279c5696fd53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667449"
---
# <a name="ipstoredeleteitem-method"></a>IPStore：:D eleteItem 方法

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

從受保護的儲存體中刪除指定的專案。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
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

**GUID** 的指標，識別要刪除之專案的資料類型。

</dd> <dt>

*pItemSubType* \[在\]
</dt> <dd>

**GUID** ，表示要刪除的專案子類型。

</dd> <dt>

*szItemName* \[在\]
</dt> <dd>

字串，其中包含要刪除之專案的名稱。

</dd> <dt>

*pPromptInfo* \[在\]
</dt> <dd>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)結構的指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定刪除操作的使用者介面和安全性行為。



| 值                                                                                                                                                                                                                                             | 意義                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_沒有任何 \_ UI \_ 遷移**</dt> <dt>0x00000010</dt> </dl> | 除非需要自訂密碼，否則不顯示使用者介面。<br/> |



 

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

 

 
