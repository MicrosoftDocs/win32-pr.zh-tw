---
description: 建立會起始其中一個所列出作業的 APDU 命令。
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'ISCardISO7816：： WriteRecord 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a023443f1121759872c4eba0743e5db5b01c8446403b312644e22c83559a527d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014378"
---
# <a name="iscardiso7816writerecord-method"></a>ISCardISO7816：： WriteRecord 方法

\[**WriteRecord** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**WriteRecord** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會起始下列其中一項作業：

-   記錄的寫入一次。
-   卡片中已有記錄資料位元組的邏輯 **OR** ，內含命令 APDU 中提供的記錄資料位元組。
-   卡片中已有記錄資料位元組的邏輯 AND，其中包含命令 APDU 中提供的記錄資料位元組。

如果資料編碼位元組中未提供任何指示，則會套用邏輯 OR 行為。

> [!Note]  
> 使用目前的記錄定址時，此命令會在已成功更新的記錄上設定記錄指標。

 

## <a name="syntax"></a>語法


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byRecordId* \[在\]
</dt> <dd>

記錄識別。 這是 P1 值：

P1 = ' 00 ' 會指定目前的記錄。

P1！ = ' 00 ' 是指定之記錄的編號。

</dd> <dt>

*byRefCtrl* \[在\]
</dt> <dd>

參考控制項 P2 的編碼。



| 值                                                                                                                                                                                                | 意義                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**目前的 EF**</dt> </dl>                     | 位位置： 00000---<br/> 目前選取的 EF。<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**簡短 EF 識別碼**</dt> </dl>                 | 位位置： xxxxx---<br/> 簡短 EF 識別碼。<br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <dt>**第一筆記錄**</dt> </dl>             | 位位置：-----000<br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <dt>**最後一筆記錄**</dt> </dl>                 | 位位置：-----001<br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <dt>**下一筆記錄**</dt> </dl>                 | 位位置：-----010<br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <dt>**上一筆記錄**</dt> </dl> | 位位置：-----011<br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <dt>**\#P1 中的記錄**</dt> </dl>    | 位位置：-----100<br/>                                   |



 

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

要寫入之記錄的指標。

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

只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。

當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。 如果在發出此命令時，目前選取了另一個基本檔案，則可能會處理此命令，而不需要識別目前選取的檔案。

如果封裝的命令套用至線性固定或迴圈結構化的基本檔案，則如果記錄長度與現有記錄的長度不同，則會中止。 如果它套用至線性變數結構化的基本檔案，則可能會在記錄長度與現有記錄的長度不同時執行。

如果 P2 = xxxxx011 且基本檔案是迴圈檔案，則此命令的行為會與使用 [**AppendRecord**](iscardiso7816-appendrecord.md)所建立的命令相同。

無法寫入沒有記錄結構的基本檔案。 如果套用至不含記錄結構的基本檔，則會中止已建立的命令。

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

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
