---
description: 建立應用程式協定資料單位 (APDU) 命令，該命令會依序將基本檔案的一部分內容設定為其邏輯清除狀態（從指定的位移開始）。
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'ISCardISO7816：： EraseBinary 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 012927e21e3ed897136a9b058ae03539b7d2e2ac0e581d04cb14235aed9ae80f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007896"
---
# <a name="iscardiso7816erasebinary-method"></a>ISCardISO7816：： EraseBinary 方法

\[**EraseBinary** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**EraseBinary** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，順序將基本檔案的一部分內容設定為其邏輯清除狀態（從指定的位移開始）。

## <a name="syntax"></a>語法


```C++
HRESULT EraseBinary(
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

RFU 位置。

如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是一個簡短的 EF 識別碼，P2 則是從檔案開頭開始，資料單位)  (清除的第一個位元組位移。

如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭)  (資料單位中清除之第一個位元組的位移。

如果資料欄位存在，則會將第一個資料單位的位移編碼為不會被清除。 此位移應高於 P1-P2 中編碼的位移。 當資料欄位為空白時，此命令會清除到檔案結尾。

</dd> <dt>

*byP2* \[在\]
</dt> <dd>

RFU 位置。

如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是一個簡短的 EF 識別碼，P2 則是從檔案開頭開始，資料單位)  (清除的第一個位元組位移。

如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭)  (資料單位中清除之第一個位元組的位移。

如果資料欄位存在，則會將第一個資料單位的位移編碼為不會被清除。 此位移應高於 P1-P2 中編碼的位移。 當資料欄位為空白時，此命令會清除到檔案結尾。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

指定清除範圍之資料的指標。 這個參數可以是 **Null**。

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會使用 *ppCmd* 指標在內部建立和傳回 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業已成功完成。<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 傳遞的參數無效。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>              |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                            |



 

## <a name="remarks"></a>備註

只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。

當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。

無法清除沒有透明結構的基本檔。 如果套用至不含透明結構的基本檔案，封裝的命令會中止。

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

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
