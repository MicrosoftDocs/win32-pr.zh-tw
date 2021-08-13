---
description: ManageChannel 方法會在開啟和關閉邏輯通道 (APDU) 命令中，建立應用程式協定資料單位。
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'ISCardISO7816：： ManageChannel 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92fb91c0630996938e247dbc244ac0c311c52531401367d5326bd197ffaabf9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481111"
---
# <a name="iscardiso7816managechannel-method"></a>ISCardISO7816：： ManageChannel 方法

\[**ManageChannel** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ManageChannel** 方法會在開啟和關閉邏輯通道 (APDU) 命令中，建立 [*應用程式協定資料單位*](../secgloss/a-gly.md)。

Open 函式會開啟基礎以外的新邏輯通道。 系統會提供卡片的選項，以指派邏輯頻道號碼，或提供給卡片的邏輯通道編號。

Close 函式會明確地關閉非基本的邏輯通道。 成功關閉之後，邏輯通道應該可供重複使用。

## <a name="syntax"></a>語法


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byChannelState* \[在\]
</dt> <dd>

P1 的 Bit b8 可用來指出 open 函式或 close 函數;如果 b8 為0，則管理通道應該會開啟邏輯通道，如果 b8 是1，則管理通道應該會關閉邏輯通道：

P1 = 要開啟的 ' 00 '

P1 = ' 80 ' 表示關閉

其他值為 RFU

</dd> <dt>

*byChannel* \[在\]
</dt> <dd>

針對開啟的函式 (P1 = ' 00 ' ) ，P2 的位 b1 和 b2 會用來以類別位元組中的相同方式來撰寫邏輯通道編號的程式碼，而 P2 的其他位則是 RFU。

當 P2 的 b1 和 b2 是 **Null** 時，卡片會指派將會在資料欄位的位 b1 和 b2 中傳回的邏輯通道編號。

當 P2 的 b1 和/或 b2 不是 **Null** 時，它們會以非基本的邏輯通道編號進行編碼;然後，卡片會開啟外部指派的邏輯頻道號碼。

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

當開啟的函式從基本邏輯通道成功執行時，應該會以隱含方式選取此 MF 作為目前的 DF，而新邏輯通道的安全性狀態應與 ATR 後的基本邏輯通道相同。 新邏輯通道的安全性狀態應與任何其他邏輯通道的安全性狀態分開。

當開啟的函式從邏輯通道（不是基本通道）成功執行時，系統會選取發出命令之邏輯通道的目前 DF 作為目前的 DF。 此外，新邏輯通道的安全性狀態應與執行 open 函式之邏輯通道的安全性狀態相同。

成功關閉函式之後，與此邏輯通道相關的安全性狀態將會遺失。

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
</dt> </dl>

 

 
