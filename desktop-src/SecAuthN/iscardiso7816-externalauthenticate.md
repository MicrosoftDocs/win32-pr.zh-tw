---
description: 建立應用程式協定資料單位 (APDU) 命令，有條件地更新安全性狀態，並在智慧卡不信任時驗證電腦的身分識別。
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'ISCardISO7816：： ExternalAuthenticate 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386170"
---
# <a name="iscardiso7816externalauthenticate-method"></a>ISCardISO7816：： ExternalAuthenticate 方法

\[**ExternalAuthenticate** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ExternalAuthenticate** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，有條件地更新安全性狀態，並在 [*智慧卡*](../secgloss/s-gly.md)不信任時驗證電腦的身分識別。

此命令會 (依據卡片先前發出的挑戰，使用 (yes 或 no) 計算的結果，例如，INS 會 \_ 取得 \_ 挑戰命令) 、金鑰 (可能秘密) 儲存在卡片中，以及由介面裝置傳輸的驗證資料。

## <a name="syntax"></a>語法


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byAlgorithmRef* \[在\]
</dt> <dd>

卡片中的演算法參考。

如果此值為零，則表示未提供任何資訊。 在發出命令或在資料欄位中提供演算法的參考時，可以知道演算法的參考。

</dd> <dt>

*bySecretRef* \[在\]
</dt> <dd>

秘密的參考。



| 值                                                                                                                                                                                    | 意義                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**沒有資訊**</dt> </dl>                     | 位位置：00000000<br/> 未提供任何資訊。 在發出命令或在 [資料] 欄位中提供秘密的參考時，就會知道秘密的參考。<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**全域參考**</dt> </dl>         | 位位置： 0-------<br/> 全域參考資料 () 的 MF 特定金鑰。<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**特定參考**</dt> </dl> | 位位置： 1-------<br/> 特定的參考資料 () 的 DF 特定索引鍵。<br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | 位位置：-xx-----<br/> 00 (其他值為 RFU) 。<br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**秘密**</dt> </dl>                         | 位位置：---xxxxx<br/> 秘密的數目。<br/>                                                                                                             |



 

</dd> <dt>

*pChallenge* \[在\]
</dt> <dd>

驗證相關資料的指標。 這個參數可以是 **Null**。

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會使用 *ppCmd* 指標在內部建立和傳回 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業已成功完成。<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 傳遞的參數無效。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>              |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                            |



 

## <a name="remarks"></a>備註

為了讓封裝的命令成功，從卡片取得的最後一項挑戰必須是有效的。

失敗的比較可能會記錄在卡片 (例如，以限制使用參考資料) 的進一步嘗試次數。

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

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
