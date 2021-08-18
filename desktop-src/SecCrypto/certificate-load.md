---
description: 從檔案匯入憑證。
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: ICertificate2：： Load 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fceb6ba9a9868711aefae64865c08e49551e20e8a05686e1691f390f05b76071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771528"
---
# <a name="icertificate2load-method"></a>ICertificate2：： Load 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**Load** 方法會從檔案匯入憑證。 此方法是在 CAPICOM 2.0 中引進。

## <a name="syntax"></a>語法


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

字串，包含包含憑證資料的 .cer 或 .pfx 檔案的路徑。

</dd> <dt>

*密碼* \[在中，選擇性\]
</dt> <dd>

字串，包含 [*私密金鑰*](../secgloss/p-gly.md)檔案的 [*明文*](../secgloss/p-gly.md)密碼。 密碼最多可包含32個 Unicode 字元，包括結束的 null 字元。 如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。

</dd> <dt>

*KeyStorageFlag* \[在中，選擇性\]
</dt> <dd>

用來定義金鑰儲存旗標之 [**CAPICOM \_ 金鑰 \_ 儲存 \_ 旗**](capicom-key-storage-flag.md) 標列舉的值。 預設值是 [CAPICOM \_ 金鑰 \_ 儲存] \_ 預設值。 下表顯示可能的值。



| 值                                                                                                                                                                                                                           | 意義                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**CAPICOM \_ 金鑰 \_ 儲存 \_ 預設值**</dt> </dl>                       | 預設金鑰存放區。<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**可 \_ 匯出的 CAPICOM 金鑰 \_ 儲存體 \_**</dt> </dl>              | 金鑰可以匯出。<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**已 \_ 保護的 CAPICOM 金鑰 \_ 儲存區 \_ 使用者 \_**</dt> </dl> | 金鑰是由使用者保護。<br/> |



 

</dd> <dt>

*KeyLocation* \[在中，選擇性\]
</dt> <dd>

定義索引鍵位置類型之 [**CAPICOM \_ 金鑰 \_ 位置**](capicom-key-location.md) 列舉的值。 預設值是 [CAPICOM \_ 目前 \_ 使用者 \_ 金鑰]。 下表顯示可能的值。



| 值                                                                                                                                                                                               | 意義                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**CAPICOM \_ 目前 \_ 使用者 \_ 金鑰**</dt> </dl>    | 金鑰是使用者金鑰。<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**CAPICOM \_ 本機 \_ 電腦 \_ 金鑰**</dt> </dl> | 金鑰是電腦金鑰。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
