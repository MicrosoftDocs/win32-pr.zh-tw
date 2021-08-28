---
description: 從檔案將憑證匯入到存放區。
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store Load 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b39c2be625ff88869d27e6210e49496352af868c73557d2657c509fd0e79f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897788"
---
# <a name="storeload-method"></a>Store Load 方法

\[**Load** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]

**Load** 方法會從檔案將憑證匯入到存放區。

## <a name="syntax"></a>語法


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

字串，其中包含 .cer、. .sst、.spc、. p7s 或 .pfx 檔案的路徑，或任何 Authenticode 簽署的檔案。

</dd> <dt>

*密碼* \[在中，選擇性\]
</dt> <dd>

字串，其中包含檔案的純文字密碼。 密碼最多可使用32個 Unicode 字元，包括結束的 null 字元。 如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。

</dd> <dt>

*KeyStorageFlag* \[在中，選擇性\]
</dt> <dd>

用來定義金鑰儲存旗標之 [**CAPICOM \_ 金鑰 \_ 儲存 \_ 旗**](capicom-key-storage-flag.md) 標列舉的值。 預設值是 [CAPICOM \_ 金鑰 \_ 儲存] \_ 預設值。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                           | 意義                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**CAPICOM \_ 金鑰 \_ 儲存 \_ 預設值**</dt> </dl>                       | 預設金鑰存放區。<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**可 \_ 匯出的 CAPICOM 金鑰 \_ 儲存體 \_**</dt> </dl>              | 金鑰可以匯出。<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**已 \_ 保護的 CAPICOM 金鑰 \_ 儲存區 \_ 使用者 \_**</dt> </dl> | 金鑰是由使用者保護。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果在記憶體存放區上呼叫 **Load** 方法，則在刪除記憶體存放區時，將會刪除任何建立的金鑰容器。 例如，如果 .pfx 檔案載入至記憶體存放區，並在稍後新增至系統存放區 (例如，從記憶體存放區) 的「我的存放區」，則「我的存放區」中的憑證將不會包含金鑰。 在此情況下，.pfx 檔案應該直接載入 My 存放區中。

\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。

如果密碼無法解密私密金鑰檔案，則應該查詢預設 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 。 如果預設 CSP 是 Microsoft 基礎密碼編譯提供者，且解密作業失敗，則應該使用 Microsoft 強式密碼編譯提供者或 Microsoft 增強型密碼編譯提供者（視何者而定），再次嘗試進行解密操作。

如果要載入到存放區中的憑證與已經存在的憑證相同， **Load** 方法將會從存放區刪除現有的憑證，然後再新增憑證。 新憑證將繼承現有憑證的屬性。 新的私密金鑰容器會取代現有的私密金鑰容器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**儲存**](store.md)
</dt> </dl>

 

 
