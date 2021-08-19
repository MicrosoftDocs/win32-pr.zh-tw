---
description: 建立應用程式協定資料單位 (APDU) 命令，此命令會使用從介面裝置送出的挑戰資料和相關的秘密 (（例如，儲存在卡片中的金鑰) ）來起始卡片的驗證資料計算。
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'ISCardISO7816：： InternalAuthenticate 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d4c3385313fb5b9c9c7ba72957244bd81757b0cd1e79bcec906e740c69b66292
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922988"
---
# <a name="iscardiso7816internalauthenticate-method"></a>ISCardISO7816：： InternalAuthenticate 方法

\[**InternalAuthenticate** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**InternalAuthenticate** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會使用從介面裝置送出的挑戰資料和相關的秘密 (（例如，儲存在卡片中的金鑰) ）來起始卡片的驗證資料計算。

當相關的秘密附加至 MF 時，命令可能會用來驗證整個卡片。

當相關的秘密附加至另一個 DF 時，命令可用來驗證該 DF。

## <a name="syntax"></a>語法


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
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



| 值                                                                                                                                                                                    | 意義                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**沒有資訊**</dt> </dl>                     | 位位置：00000000 <br/> 未提供任何資訊。 在發出命令或在 [資料] 欄位中提供秘密的參考時，就會知道秘密的參考。<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**全域參考**</dt> </dl>         | 位位置： 0------- <br/> 全域參考資料 () 的 MF 特定金鑰。<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**特定參考**</dt> </dl> | 位位置： 1-------<br/> 特定的參考資料 () 的 DF 特定索引鍵。<br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | 位位置：-xx-----<br/> 00 (其他值為 RFU) 。<br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**秘密**</dt> </dl>                         | 位位置：---xxxxx<br/> 秘密的數目。<br/>                                                                                                              |



 

</dd> <dt>

*pChallenge* \[在\]
</dt> <dd>

驗證相關資料的指標 (例如，挑戰) 。

</dd> <dt>

*lReplyBytes* \[在\]
</dt> <dd>

回應中預期的最大位元組數目。

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並使用 *ppCmd* 指標來傳回。

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

成功執行命令可能會受到先前命令的成功完成 (例如，確認或選取檔案) 或選取 (例如) 相關的秘密。

如果在發出命令時目前已選取金鑰和演算法，則命令可以隱含地使用金鑰和演算法。

發出命令的次數可能會記錄在卡片中，以限制使用相關密碼或演算法的進一步嘗試次數。

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

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
