---
description: 在目前的捕獲內容中尋找符合篩選準則的下一個畫面格。
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: 'FindNextFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510979"
---
# <a name="findnextframe-function"></a>FindNextFrame 函式

**FindNextFrame** 函式會在目前的捕獲內容中尋找符合篩選準則的下一個畫面格。

## <a name="syntax"></a>語法


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
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

目的地位址。

</dd> <dt>

*SourceAddress* 
</dt> <dd>

來源位址。

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

將接收通訊協定位移的 **單字** 指標。

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

搜尋的起點。 根據預設，此函式會從 *OriginalFrameNumber* 起點搜尋向前1000的畫面格。 若要變更向前搜尋的距離，請將這一行新增至位於網路監視器目錄中的 Nmapi.ini 檔案 \\ 。

MAXLOOKBACK =<new lookforward distance>

</dd> <dt>

*HighestFrame* 
</dt> <dd>

在捕捉中搜尋的最大框架編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是下一個框架的控制碼。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

Capture 篩選器主要由 *ProtocolName* 參數定義，這是唯一必要的篩選輸入;您可以新增 *DestinationAddress* 和 *SourceAddress* 資料，以提高捕獲速度。

*ProtocolOffset* 指標會傳回給呼叫剖析器，它會使用 [ParserTemporaryLockFrame](parsertemporarylockframe.md)) 來鎖定框架 (，以將該 **字** 組新增至所傳回的指標，以取得所搜尋的通訊協定 **LPBYTE** 。 傳回時，傳遞篩選器的 HFRAME 會提供給剖析器。 如果剖析器發現這個框架不是搜尋的畫面格，剖析器可以將 HFRAME 交給 **FindNextFrame** 函式，以取得下一個畫面格。 來源和目的地位址不是必要的，而且可以傳遞為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




