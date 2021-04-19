---
description: 在離線登錄 hive 中建立指定的登錄機碼。 如果索引鍵已經存在，則函式會將它開啟。
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: 'ORCreateKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991339"
---
# <a name="orcreatekey-function"></a>ORCreateKey 函式

在離線登錄 hive 中建立指定的登錄機碼。 如果索引鍵已經存在，則函式會將它開啟。

## <a name="syntax"></a>語法


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*lpSubKey* \[在\]
</dt> <dd>

包含此函式開啟或建立之子機碼名稱的 Unicode 字串指標。 *LpSubKey* 參數必須指定 *Handle* 參數所識別之機碼的子機碼;在登錄樹狀目錄中，最多可以有32層級的深度。 如需索引鍵名稱的詳細資訊，請參閱登錄 [結構](../sysinfo/structure-of-the-registry.md)。

此參數不可以是 **Null**。

索引鍵名稱不區分大小寫。

</dd> <dt>

*lpClass* \[在中，選擇性\]
</dt> <dd>

類別 (此索引鍵) 物件類型。 您可以忽略這個參數。 此參數可以是 **Null**。

</dd> <dt>

*>dwoptions* \[在中，選擇性\]
</dt> <dd>

此參數可以是0或下列其中一個值。



| 值                                                                                                                                                                                                                                                          | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**REG \_選項 \_ 建立 \_ 連結**</dt> <dt>0x00000002L</dt> </dl>    | 索引鍵是符號連結。 目標路徑會指派給機碼的 L "SymbolicLinkValue" 值。 目標路徑必須是絕對登錄路徑。 如果設定此選項，則也必須設定 **REG \_ 選項 \_ 非 \_ VOLATILE** 。 <br/> 如果 *lpSubKey* 參數指定現有的金鑰，就必須使用 **REG \_ OPTION \_ CREATE \_ LINK** 來建立它。<br/> 只有在應用程式相容性絕對必要時，才應該使用登錄符號連結。 <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**REG \_選項 \_ 非 \_ VOLATILE**</dt> <dt>0x00000000L</dt> </dl> | 金鑰不是 volatile;這是預設值。 這項資訊會儲存在檔案中，並在系統重新開機時予以保留。 [**ORSaveHive**](orsavehive.md)函式會儲存非 volatile 的索引鍵。<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[在中，選擇性\]
</dt> <dd>

[安全 \_ 描述項](/windows/win32/api/winnt/ns-winnt-security_descriptor)結構的指標，其中包含新金鑰的安全描述項。 如果 *pSecurityDescriptor* 為 **Null**，則索引鍵會取得預設安全描述項。 金鑰之預設安全描述項中的 Acl 會從其直接父機碼繼承。

</dd> <dt>

*phkResult* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收開啟或建立之索引鍵的控制碼。 當您完成使用控制碼之後，請使用 [**ORCloseKey**](orclosekey.md) 函數來關閉金鑰。

</dd> <dt>

*pdwDisposition* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收下列其中一個配置值。



| 值                                                                                                                                                                                                                                                          | 意義                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**REG \_已建立 \_ 新的 \_ 金鑰**</dt> <dt>0x00000001L</dt> </dl>             | 金鑰不存在且已建立。<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**REG \_開啟 \_ 現有的 \_ 金鑰**</dt> <dt>0x00000002L</dt> </dl> | 金鑰已存在，而且只會在未變更的情況下開啟。<br/> |



 

如果 *pdwDisposition* 為 **Null**，則不會傳回任何處置資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

如果 *>dwoptions* 參數是以 **REG \_ 選項 \_ CREATE \_ LINK** 設定，但 **reg \_ 選項 \_ \_** 為 clear，或是要傳回的控制碼是 hive 的根目錄控制碼，則函式會傳回錯誤 \_ 不正確 \_ 參數。

## <a name="remarks"></a>備註

**ORCreateKey** 函數所建立的索引鍵沒有值。 應用程式可以使用 [**ORSetValue**](orsetvalue.md) 函數來設定索引鍵值。

**ORCreateKey** 函式不能用來在離線登錄 hive 中建立根金鑰。 您可以使用 [**ORCreateHive**](orcreatehive.md) 函式來建立根金鑰，並取得索引鍵的控制碼。

離線登錄不支援儲存個別的金鑰。 使用 [**ORSaveHive**](orsavehive.md) 函式，將索引鍵和其子機碼儲存在 hive 中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[安全 \_ 描述項](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
