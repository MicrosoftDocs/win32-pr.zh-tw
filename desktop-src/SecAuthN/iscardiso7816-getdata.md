---
description: 使用的方法會將應用程式協定資料單位 (APDU) 命令，以根據所選取的檔案類型，抓取單一基本資料物件或 (包含在結構化) 資料物件中的一組資料物件。
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'ISCardISO7816：： Scardssp 方法 (.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694039"
---
# <a name="iscardiso7816getdata-method"></a>ISCardISO7816：：：：的方法

\[您可以在 [需求] 區段中指定的作業系統中使用 [ **操作方法]** 。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

使用 **的** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，以根據所選取的檔案類型，抓取單一基本資料物件或 (包含在結構化) 資料物件中的一組資料物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byP1* \[在\]
</dt> <dd>

參數。



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

參數。



| 值                                                                                  | 意義                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | BER-TLV 標記 (1 位元組) 在 P2 中<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | 應用程式資料 (專屬編碼) <br/> |
| <dl> <dt>0200-02FF</dt> </dl> | P2 中的簡單 TLV 標記<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV 標記 (2 個位元組) 在 P1-P2 中<br/>        |



 

</dd> <dt>

*lBytesToGet* \[在\]
</dt> <dd>

回應中預期的位元組數目。

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

只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所讀取之基本檔案的安全性屬性時，才能執行封裝的命令。 安全性條件取決於卡片的原則，並可透過 [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)、 [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)、 [**ISCardAuth**](iscardauth.md)等操作。

若要選取檔案，請呼叫 [**SelectFile**](iscardiso7816-selectfile.md)。

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

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**PutData**](iscardiso7816-putdata.md)
</dt> <dt>

[**SelectFile**](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
