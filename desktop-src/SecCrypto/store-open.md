---
description: 開啟指定的憑證存放區。
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Store. Open 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d70c6410d0ecb8edb91aa722bcf6f35cb9536c3ed2b7f03c2d5cb141937aeb69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897801"
---
# <a name="storeopen-method"></a>Store. Open 方法

\[**Open** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]

**Open** 方法會開啟指定的 [*憑證存放區*](../secgloss/c-gly.md)。 根據預設，會以 \_ \_ 唯讀方式開啟 capicom 目前的使用者 \_ 存放區位置和 capicom \_ MY \_ store 存放區。

## <a name="syntax"></a>語法


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*StoreLocation* \[在中，選擇性\]
</dt> <dd>

[CAPICOM \_ 存放區 \_ 位置](capicom-store-location.md)列舉的值，指出要開啟之存放區的位置。 預設值是 [CAPICOM \_ 目前 \_ 使用者 \_ 存放區]。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 使用者 \_ 存放區**</dt> </dl> | 存放區是 Active Directory 存放區。 如果 Active Directory 存放區開啟為讀取/寫入，則不會產生任何錯誤，但不會保存存放區的任何變更。 憑證無法在 Active Directory 存放區中新增或移除。<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**CAPICOM \_ 目前的 \_ 使用者 \_ 存放區**</dt> </dl>                             | 存放區是目前的使用者存放區。 目前的使用者存放區可能是「讀取/寫入」存放區。 如果是，就會保存存放區內容中的變更。<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**CAPICOM \_ 本機 \_ 電腦 \_ 存放區**</dt> </dl>                          | 存放區是本機電腦存放區。 只有當使用者擁有讀取/寫入權限時，本機電腦存放區才可以是讀取/寫入存放區。 如果使用者具有讀取/寫入權限，且存放區已開啟讀取/寫入，則會保存存放區內容中的變更。<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**CAPICOM \_ 記憶體 \_ 存放區**</dt> </dl>                                                | 存放區是記憶體存放區。 存放區內容中的任何變更都不會保存。<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**CAPICOM \_ 智慧 \_ 卡 \_ 使用者 \_ 存放區**</dt> </dl>                   | 存放區是一組目前的智慧卡。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[在中，選擇性\]
</dt> <dd>

字串，包含要開啟之系統憑證存放區的名稱。 預設值是 [CAPICOM \_ 我的 \_ 存放區]。 如果從 web 腳本開啟存放區， \\ 名稱中不允許使用反斜線 () 字元。 除了系統所定義的存放區之外，還可以開啟使用者定義存放區。

這個參數可以是使用者定義的存放區，也可以是下列其中一個系統憑證存放區。



| 值                                                                                                                                                                            | 意義                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**CAPICOM \_ CA \_ 存放區**</dt> </dl>          | CA 存放區。 此存放區是用來儲存中繼 CA 憑證。<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ 我的 \_ 存放區**</dt> </dl>          | 我的存放區。 此存放區會用於使用者的個人憑證。<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**CAPICOM \_ 其他 \_ 存放區**</dt> </dl> | AddressBook 存放區。 此存放區是用來保留其他人的憑證。<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**CAPICOM \_ 根 \_ 存放區**</dt> </dl>    | 根存放區。 此存放區是用來儲存根 CA 和自我簽署的受信任憑證。<br/> |



 

</dd> <dt>

*OpenMode* \[在中，選擇性\]
</dt> <dd>

表示存放區開啟模式之 [CAPICOM \_ 存放區 \_ 開啟 \_ 模式](capicom-store-open-mode.md) 列舉的值。 預設值是 [CAPICOM \_ 存放區 \_ 開啟 \_ 唯讀] \_ 。 如果從 web 腳本開啟存放區，則會強制將這個值強制設 \_ 為 \_ 僅限開放式儲存區 \_ \_ 。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                           | 意義                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**允許的 CAPICOM \_ 存放區 \_ 開啟 \_ 上限 \_**</dt> </dl> | 如果使用者具有讀取/寫入權限，請以讀取/寫入模式開啟存放區。否則，請在唯讀模式中開啟存放區。<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**CAPICOM \_ 存放區 \_ 開啟 \_ 唯讀 \_**</dt> </dl>                   | 在唯讀模式開啟存放區。<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**CAPICOM \_ 存放區 \_ 開啟 \_ 讀 \_ 寫**</dt> </dl>                | 以讀取/寫入模式開啟存放區。<br/>                                                                                     |



 

下列旗標可以使用邏輯 **OR** 運算，與上表中的值結合。



| 值                                                                                                                                                                                                                              | 意義                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**CAPICOM \_ 存放 \_ 區 \_ 僅開啟現有 \_ 的**</dt> </dl>          | 僅開啟現有的商店;請勿建立新的存放區。 在 CAPICOM 2.0 中引進。<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**開啟的 CAPICOM \_ 存放區 \_ \_ 包含 \_ 封存**</dt> </dl> | 使用存放區時，請包含封存的憑證。 在 CAPICOM 2.0 中引進。<br/>   |



 

某些位置中的存放區只能在唯讀模式中開啟。 這些包含在 CAPICOM \_ 本機 \_ 電腦 \_ 存放區中，使用者沒有寫入權限的所有存放區。 如果沒有適當的存取權和許可權，嘗試以讀取/寫入存放區的形式開啟存放區，將會導致 **open** 方法失敗。 Active Directory 存放區可以開啟為讀取/寫入存放區，而不會導致 **Open** 方法失敗，但將不會保存存放區的變更。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果在智慧卡存放區上呼叫這個方法，可能會叫用額外的智慧卡使用者介面。

> [!IMPORTANT]
> 從 web 腳本呼叫這個方法時，腳本必須存取本機電腦上的數位憑證。 如果您允許腳本存取您的數位憑證，執行腳本的網站也可以存取儲存在憑證中的任何個人資訊。 第一次從特定網域呼叫這個方法時，會產生一個對話方塊，使用者必須在此對話方塊中指出是否允許存取憑證。 從 web 腳本開啟的存放區會自動強制將 CAPICOM \_ 存放區設為 \_ 開放式 \_ 現有的旗標 \_ 。

 

如果 *StoreLocation* 為 **CAPICOM \_ 智慧 \_ 卡 \_ 使用者 \_ 存放區**，則會忽略 *StoreName* 。 在此情況下，CAPICOM 會讀取所有包含智慧卡之可用讀取器的憑證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**儲存**](store.md)
</dt> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**關閉**](store-close.md)
</dt> </dl>

 

 
