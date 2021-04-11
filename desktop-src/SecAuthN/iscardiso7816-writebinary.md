---
description: WriteBinary 方法會建立應用程式協定資料單位 (APDU) 命令，以將二進位值寫入基本檔案。
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'ISCardISO7816：： WriteBinary 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936609"
---
# <a name="iscardiso7816writebinary-method"></a>ISCardISO7816：： WriteBinary 方法

\[**WriteBinary** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**WriteBinary** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，以將二進位值寫入基本檔案。

視檔案屬性而定，此命令會執行下列其中一項作業：

-   包含在命令 APDU 中的位的邏輯 OR 已存在於命令 APDU (邏輯清除的檔案位狀態為 0) 。
-   包含在命令 APDU 中的位的邏輯 AND 都已存在於命令 APDU (邏輯清除的檔案位狀態為 1) 。
-   在命令 APDU 中指定之位的卡片中進行一次性寫入。

如果資料編碼位元組中未提供任何指示，則會套用邏輯 OR 行為。

## <a name="syntax"></a>語法


```C++
HRESULT WriteBinary(
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

從二進位檔案開頭的寫入位置位移 (EF) 。 如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 是從檔案開頭以資料單位寫入的第一個位元組位移。 如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭以資料單位寫入之第一個位元組的位移。

</dd> <dt>

*byP2* \[在\]
</dt> <dd>

從二進位檔案開頭的寫入位置位移 (EF) 。 如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 是從檔案開頭以資料單位寫入的第一個位元組位移。 如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭以資料單位寫入之第一個位元組的位移。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

要寫入之資料單位的字串指標。

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。

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

只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。

當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。

當寫入二進位運算已套用至一次性寫入 EF 的資料單位時，如果任何附加至此資料單位的) 與邏輯清除的狀態不同，則會在資料單位或邏輯清除狀態指標的內容 (時，中止任何參考此資料單位的寫入作業。

無法寫入不含透明結構的基本檔案。 如果套用至不含透明結構的基本檔案，封裝的命令會中止。

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

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
