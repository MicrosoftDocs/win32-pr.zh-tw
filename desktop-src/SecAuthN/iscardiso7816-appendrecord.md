---
description: AppendRecord 方法會將應用程式協定資料單位 (APDU) 命令，將記錄附加至線性結構化基礎檔案的結尾 (EF) 或在迴圈結構化的基本檔案中寫入記錄號碼1。
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: 'ISCardISO7816：： AppendRecord 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: de2b6ac4bfded1612713272111f3ef21f21cf4b7b8ac9cedae769531fee26c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923059"
---
# <a name="iscardiso7816appendrecord-method"></a>ISCardISO7816：： AppendRecord 方法

\[**AppendRecord** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**AppendRecord** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，將記錄附加至線性結構化基礎檔案的結尾 (EF) 或在迴圈結構化的基本檔案中寫入記錄號碼1。

## <a name="syntax"></a>語法


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byRefCtrl* \[在\]
</dt> <dd>

識別要附加的基本檔。



| 值                                                                                                                                                                                | 意義                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**目前的 EF**</dt> </dl>     | 位位置：00000000<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**簡短 EF 識別碼**</dt> </dl> | 位位置： xxxxx000<br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**保留**</dt> </dl>             | 位位置： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx<br/> |



 

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

要附加至檔案的資料指標。



| 值                                                                                                                                                | 意義                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <dt>**Tn**</dt> </dl>     | 1 個位元組<br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <dt>**Ln**</dt> </dl> | 1或3個位元組<br/> |
| <span id="data"></span><span id="DATA"></span><dl> <dt>**資料**</dt> </dl>                    | Ln 位元組<br/>     |



 

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會使用 *ppCmd* 指標在內部建立和傳回 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md)物件。

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

只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合讀取之基本檔案的安全性屬性時，才能執行封裝的命令。

如果在發出此命令時選取了另一個基本檔案，則可能會在未識別目前選取的檔案的情況下進行處理。

無法讀取沒有記錄結構的基本檔案。 如果套用至不含記錄結構的基本檔案，封裝的命令會中止。

如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardsrv .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
