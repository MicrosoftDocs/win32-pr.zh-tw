---
description: UpdateBinary 方法會將應用程式協定資料單位 (APDU) 命令，以使用 APDU 命令中指定的位來更新基本檔案中的位。
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: 'ISCardISO7816：： UpdateBinary 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d9651189cab228eaa5dacc9c2f5963201bbc65c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980339"
---
# <a name="iscardiso7816updatebinary-method"></a>ISCardISO7816：： UpdateBinary 方法

\[**UpdateBinary** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**UpdateBinary** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，以使用 APDU 命令中指定的位來更新基本檔案中的位。

## <a name="syntax"></a>語法


```C++
HRESULT UpdateBinary(
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

寫入的位移 (從二進位檔開頭將) 位置更新為二進位檔。 如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 則是從檔案開頭開始更新資料單位的第一個位元組位移。 如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭開始更新資料單位中第一個位元組的位移。

</dd> <dt>

*byP2* \[在\]
</dt> <dd>

寫入的位移 (從二進位檔開頭將) 位置更新為二進位檔。 如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 則是從檔案開頭開始更新資料單位的第一個位元組位移。 如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭開始更新資料單位中第一個位元組的位移。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

要更新之資料單位的字串指標。

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

只有當智慧卡的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。

當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。

無法清除沒有透明結構的基本檔。 如果套用至不含透明結構的基本檔案，封裝的命令會中止。

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

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
