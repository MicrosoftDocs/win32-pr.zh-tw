---
description: 建立應用程式協定資料單位 (APDU) 命令，此命令會使用卡片中儲存的參考資料，從介面裝置所傳送的驗證資料) 中起始比較 ( (例如，密碼) 。
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'ISCardISO7816：： Verify 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980338"
---
# <a name="iscardiso7816verify-method"></a>ISCardISO7816：： Verify 方法

\[[ **驗證** ] 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Verify** 方法會 (APDU 來建立 [*應用程式協定資料單位*](../secgloss/a-gly.md)) 命令，以在從介面裝置傳送的驗證資料) 中，使用儲存在卡片中的參考資料來啟動 (的驗證資料 (例如，密碼) 。

## <a name="syntax"></a>語法


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byRefCtrl* \[在\]
</dt> <dd>

參考資料的數量詞。 參考控制項 P2 的編碼如下。

當主體是空的時，您可以使用此命令來取得進一步允許的重試次數 (SW1-SW2 = 63CX) 或檢查是否不需要驗證 (SW1-SW2 = 9000) 。



| 值                                                                                                                                                                                    | 意義                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**沒有資訊**</dt> </dl>                     | 位位置：00000000<br/> P2 = 00 是保留的，表示在這些卡片中不會使用任何特定的辨識符號，而驗證命令會明確地參考秘密資料。<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**全域參考**</dt> </dl>         | 位位置： 0-------<br/> 全域 Ref 的範例就是密碼。<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**特定參考**</dt> </dl> | 位位置： 1-------<br/> 特定 Ref 的範例是 DF 特定密碼。<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | 位位置：-xx-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**參考資料 \#**</dt> </dl>        | 位位置：---xxxxx<br/> 例如，參考資料編號可能是密碼號碼或簡短的 EF 識別碼。<br/>                                                           |



 

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

驗證資料的指標。 此參數可以是 **Null**。 預設值是 **NULL**。

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會使用 *ppCmd* 指標在內部建立和傳回 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業已成功完成。<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 使用了不正確參數。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                          |



 

## <a name="remarks"></a>備註

可能會因為比較結果而修改安全性狀態。 失敗的比較可能會記錄在卡片 (例如，以限制使用參考資料) 的進一步嘗試次數。

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
