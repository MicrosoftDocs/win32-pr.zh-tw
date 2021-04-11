---
description: FindPreviousFrame 函式會在目前的捕獲內容中尋找符合篩選準則的上一個畫面格。
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: 'FindPreviousFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936633"
---
# <a name="findpreviousframe-function"></a>FindPreviousFrame 函式

**FindPreviousFrame** 函式會在目前的捕獲內容中尋找符合篩選準則的上一個畫面格。

## <a name="syntax"></a>語法


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCurrentFrame* 
</dt> <dd>

框架的控制碼。

</dd> <dt>

*ProtocolName* 
</dt> <dd>

通訊協定名稱，例如 TCP。

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

搜尋之框架的目的地位址。

</dd> <dt>

*SourceAddress* 
</dt> <dd>

搜尋之框架的來源位址。

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

接收通訊協定位移的 **單字** 指標。

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

搜尋起點。 根據預設，此函式會從 *OriginalFrameNumber* 起始點搜尋反向1000的畫面格。 您可以藉由將這一行新增至 Nmapi.ini 檔案（位於網路監視器目錄中），來變更搜尋後距離 \\ 。

MAXLOOKBACK =<new lookback distance>

</dd> <dt>

*LowestFrame* 
</dt> <dd>

所搜尋之捕捉中的最小框架編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是上一個框架的控制碼。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

Capture 篩選器主要是由 *ProtocolName* 所定義，這是唯一需要的篩選器輸入;您可以新增 *DestinationAddress* 和 *SourceAddress* 資訊來提高捕捉速度。

*ProtocolOffset* 會傳回給呼叫剖析器，它會將此 **DWORD** 新增至透過 [ParserTemporaryLockFrame](parsertemporarylockframe.md)) 鎖定框架 (所傳回的指標，以取得所搜尋之通訊協定的 LPBYTE。 傳回時，傳遞篩選器的 HFRAME 會提供給剖析器。 如果剖析器發現框架不是正在搜尋的框架，剖析器可以將這個 HFRAME 交給 **FindPreviousFrame** 函式，以取得下一個畫面格。 來源和目的地位址（非必要）可以傳入做為 **Null**。 使用時，這些位址可以是類型的 \_ IP 位址 \_ ，而不只是 MAC 類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




