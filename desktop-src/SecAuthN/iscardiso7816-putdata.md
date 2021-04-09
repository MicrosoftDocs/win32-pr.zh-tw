---
description: PutData 方法會建立應用程式協定資料單位 (APDU) 命令，此命令會根據選取的檔案，儲存單一基本資料物件或包含在結構化資料物件中的資料物件集。
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: 'ISCardISO7816：:P utData 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850880"
---
# <a name="iscardiso7816putdata-method"></a>ISCardISO7816：:P utData 方法

\[**PutData** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**PutData** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會根據選取的檔案，儲存單一基本資料物件或包含在結構化資料物件中的資料物件集。

物件的儲存方式 (寫入一次和（或）更新和/或附加) 取決於資料物件的定義或本質。

## <a name="syntax"></a>語法


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byP1* \[在\]
</dt> <dd>

P1-P2 的編碼。



| 值                                                                                  | 意義                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | BER-TLV 標記 (1 位元組) 在 P2 中<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | 應用程式資料 (專屬編碼) <br/> |
| <dl> <dt>0200-02FF</dt> </dl> | P2 中的簡單 TLV 標記<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV 標記 (2 個位元組) 在 P1-P2 中<br/>        |



 

</dd> <dt>

*byP2* \[在\]
</dt> <dd>

P1-P2 的編碼。



| 值                                                                                  | 意義                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | BER-TLV 標記 (1 位元組) 在 P2 中<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | 應用程式資料 (專屬編碼) <br/> |
| <dl> <dt>0200-02FF</dt> </dl> | P2 中的簡單 TLV 標記<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV 標記 (2 個位元組) 在 P1-P2 中<br/>        |



 

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

位元組緩衝區的指標，其中包含要寫入的參數和資料。

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並使用 *ppCmd* 指標來傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

只有在安全性狀態符合函式 [*內容*](../secgloss/c-gly.md) 中的應用程式所定義的安全性條件時，才能執行此命令。

<dl> <dt>

<span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>儲存應用程式資料
</dt> <dd>

當 P1-P2 的值位於0100至01FF 的範圍內時，P1-P2 的值應該是針對卡片內部測試所保留的識別碼，以及在指定的應用程式內容中有意義的專屬服務。

</dd> <dt>

<span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>儲存資料物件
</dt> <dd>

當值 P1-P2 位於0040至00FF 的範圍內時，P2 的值應該是單一位元組上的 BER TLV 標記。 00FF 的值是保留的，表示資料欄位攜帶 BER 的 TLV 資料物件。

當 P1-P2 的值位於0200至02FF 的範圍時，P2 的值應該是簡單的 TLV 標記。 值0200為 RFU。 值02FF 會保留，表示資料欄位會攜帶簡單的 TLV 資料物件。

當 P1-P2 的值位於4000至 FFFF 的範圍內時，P1-P2 的值應該是兩個位元組上的 BER TLV 標記。 RFU 的值為4000至 FFFF。

當提供基本資料物件時，命令訊息的資料欄位應該會包含對應基本資料物件的值。

當提供了結構化資料物件時，命令訊息的資料欄位應該會包含已建立的資料物件值 (也就是資料物件，包括其標記、長度和值) 。

</dd> </dl>

如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardsrv .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetData**](iscardiso7816-getdata.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
