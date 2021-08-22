---
description: ReadRecord 方法會建立應用程式協定資料單位 (APDU) 命令，以讀取指定記錄的內容或基本檔案的一筆記錄的開頭部分。
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'ISCardISO7816：： ReadRecord 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 16edb529cb5a1cf6e2badd19c3ac37f1e7ec69649fb854f98ff0b515c573f874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141081"
---
# <a name="iscardiso7816readrecord-method"></a>ISCardISO7816：： ReadRecord 方法

\[**ReadRecord** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ReadRecord** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，以讀取指定記錄的內容或基本檔案的一筆記錄的開頭部分。

## <a name="syntax"></a>語法


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byRecordId* \[在\]
</dt> <dd>

要讀取之第一筆記錄的記錄號碼或識別碼 (00 表示目前的記錄) 。

</dd> <dt>

*byRefCtrl* \[在\]
</dt> <dd>

參考控制項的編碼。



| 值                                                                                                                                                                                | 意義                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**目前的 EF**</dt> </dl>     | 位位置： 00000---<br/> 目前選取的 EF。<br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**簡短 EF 識別碼**</dt> </dl> | 位位置： xxxxx---<br/> 簡短 EF 識別碼。<br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | 位位置： 11111---<br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <dt>**記錄 \#**</dt> </dl>            | 位位置：-----1xx<br/> P1 中記錄號碼的使用量。<br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <dt>**讀取記錄**</dt> </dl> | 位位置：-----100<br/> 讀取記錄 P1。<br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <dt>**最高到最後**</dt> </dl>     | 位位置：-----101<br/> 從 P1 讀取所有記錄到最後一個。 <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <dt>**最多 P1**</dt> </dl>             | 位位置：-----110<br/> 讀取從最多到 P1 的所有記錄。 <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | 位位置：-----111<br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <dt>**記錄識別碼**</dt> </dl>         | 位位置：-----0xx<br/> P1 中記錄號碼的使用量。<br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <dt>**第一次發生**</dt> </dl> | 位位置：-----000<br/> 讀取首次發生。 <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <dt>**上次發生時間**</dt> </dl>     | 位位置：-----001<br/> 讀取最後一個出現的專案。 <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <dt>**下次發生**</dt> </dl>     | 位位置：-----010<br/> 讀取下一個出現的專案。 <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <dt>**上一個**</dt> </dl>             | 位位置：-----011<br/> 讀取先前的出現專案。 <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**秘密**</dt> </dl>                     | 位位置：---xxxxx<br/>                                                      |



 

</dd> <dt>

*lBytesToRead* \[在\]
</dt> <dd>

要從透明 EF 讀取的位元組數目。

如果 Le 欄位只包含零，則根據 P2 的 b3b2b1，以及在256的長度下限或65536（延長長度），此命令應完全讀取單一要求的記錄或要求的記錄順序。

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所讀取之基本檔案的安全性屬性時，才能執行封裝的命令。

如果在發出此命令時，目前選取了另一個基本檔案，則可能會在未識別目前選取的檔案的情況下進行處理。

當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。

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

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
