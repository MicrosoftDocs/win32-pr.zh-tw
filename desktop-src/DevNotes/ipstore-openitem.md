---
description: 開啟多個存取的專案。
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'IPStore：： OpenItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999988"
---
# <a name="ipstoreopenitem-method"></a>IPStore：： OpenItem 方法

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

開啟多個存取的專案。

## <a name="syntax"></a>語法


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
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

*pItemType* \[在\]
</dt> <dd>

GUID 的指標，識別要開啟之專案的資料類型。

</dd> <dt>

*pItemSubtype* \[在\]
</dt> <dd>

GUID 的指標，指出要開啟的專案子類型。

</dd> <dt>

*szItemName* \[在\]
</dt> <dd>

字串，包含要開啟之專案的名稱。

</dd> <dt>

*ModeFlags* \[在\]
</dt> <dd>

描述指定的一組存取子句所適用的存取模式。 如需詳細資訊，請參閱 [**PStore 類型**](pstore-types.md)。



| 值                                                                                                                                                                                                         | 意義                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_讀取**</dt> <dt>0x0001</dt> </dl>    | 讀取存取模式。<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_寫入**</dt> <dt>0x0002</dt> </dl> | 寫入存取模式。<br/> |



 

</dd> <dt>

*pProomptInfo* \[在\]
</dt> <dd>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)結構的指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

Reserved：必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT** 值。 值為 **PST \_ E \_ OK** 表示函式已成功。

## <a name="remarks"></a>備註

使用 **OpenItem** 在受保護的儲存體資料庫中開啟專案時，需要最後使用 [**IPStore：： CloseItem**](ipstore-closeitem.md) 來關閉專案，以避免記憶體流失。

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

 

 
