---
description: GetResponse 方法會建立應用程式協定資料單位 (APDU) 命令，此命令會將 APDU 命令傳輸 (或部分的 APDU 命令) 否則無法由可用的通訊協定傳輸。
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: 'ISCardISO7816：： GetResponse 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0b74fe9620aefc390957b88f9cf286f7871c1d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985002"
---
# <a name="iscardiso7816getresponse-method"></a>ISCardISO7816：： GetResponse 方法

\[**GetResponse** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**GetResponse** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會將 apdu 命令傳輸 (或部分的 apdu 命令) 否則無法由可用的通訊協定傳輸。

## <a name="syntax"></a>語法


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byP1* \[在\]
</dt> <dd>

根據 ISO 7816-4，P1 應該是零 (RFU) 。

</dd> <dt>

*byP2* \[在\]
</dt> <dd>

根據 ISO 7816-4，P2 應該是零 (RFU) 。

</dd> <dt>

*lDataLength* \[在\]
</dt> <dd>

傳送的資料長度。

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

 

 
