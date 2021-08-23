---
description: RecognizeFrame export 函數會指出是否要將資料片段辨識為剖析器偵測到的通訊協定。 必須針對剖析器 DLL 支援的每個剖析器，執行 RecognizeFrame 匯出函數。
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: 'RecognizeFrame 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: b9f8fcbfccdb306038b7b654e947ff1a11654267012c7527799d8633ed8a9410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889698"
---
# <a name="recognizeframe-callback-function"></a>RecognizeFrame 回呼函式

**RecognizeFrame** export 函數會指出是否要將資料片段辨識為剖析器偵測到的通訊協定。 必須針對剖析器 DLL 支援的每個剖析器，執行 **RecognizeFrame** 匯出函數。

## <a name="syntax"></a>語法


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

包含資料之框架的控制碼。

</dd> <dt>

*lpFrame* \[在\]
</dt> <dd>

框架第一個位元組的指標。 指標會提供一種方式來查看其他剖析器辨識的資料。

</dd> <dt>

*lpProtocol* \[在\]
</dt> <dd>

取消認領資料開頭的指標。 一般而言，取消認領資料是位於框架的中間，因為先前的剖析器已在此剖析器之前宣告資料。 剖析器必須先測試取消認領的資料。

</dd> <dt>

*MacType* \[在\]
</dt> <dd>

框架中第一個通訊協定的 MAC 值。 一般來說，當剖析器必須識別框架中的第一個通訊協定時，就會使用 *MacType* 值。 *MacType* 值可以是下列其中一項：



| 值                                                                                                                                                                         | 意義                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**MAC \_ 類型 \_ ETHERNET**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**MAC \_ 類型 \_ TOKENRING**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**MAC \_ 類型的 \_ FDDI**</dt> </dl>                | ANSI X3T 9。5 <br/> |



 

</dd> <dt>

*BytesLeft* \[在\]
</dt> <dd>

從框架位置到框架結尾的剩餘位元組數目。

</dd> <dt>

*hPreviousProtocol* \[在\]
</dt> <dd>

先前通訊協定的控制碼。

</dd> <dt>

*nPreviousProtocolOffset* \[在\]
</dt> <dd>

框架開頭的先前通訊協定位移。

</dd> <dt>

*ProtocolStatusCode* \[擴展\]
</dt> <dd>

通訊協定狀態指標。 剖析器 DLL 必須設定下列其中一個狀態碼。



| 值                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**識別的通訊協定 \_ 狀態 \_**</dt> </dl>              | 剖析器會辨識資料，但不知道接下來的通訊協定。 設定完程式碼之後，請將指標傳回至遵循辨識通訊協定的其餘取消認領資料。 網路監視器會使用 [*下列一組*](f.md) 通訊協定來繼續剖析。 <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**無法辨識通訊協定 \_ 狀態 \_ \_**</dt> </dl> | 剖析器無法辨識資料。 設定此程式碼之後，請使用 *lpProtocol* 參數傳遞至剖析器 DLL 的指標，將指標傳回至資料的開頭。 網路監視器使用先前的通訊協定 *集合* 來繼續剖析。 <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**已宣告的通訊協定 \_ 狀態 \_**</dt> </dl>                       | 剖析器會辨識資料並宣告剩餘的資料。 設定程式碼之後，請針對網路監視器傳回 **Null** ，以終止剖析框架。 <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**通訊協定 \_ 狀態 \_ 下一個 \_ 通訊協定**</dt> </dl>    | 剖析器會辨識資料並知道接下來的通訊協定。 設定程式碼之後，請設定 *phNextProtocol* 參數，並將指標傳回其餘的取消認領資料，並遵循辨識的通訊協定。 網路監視器會繼續剖析框架。 <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[擴展\]
</dt> <dd>

下一個通訊協定的控制碼指標。 當通訊協定識別遵循通訊協定的通訊協定時，就會設定此參數。 若要取得下一個通訊協定的控制碼，請呼叫 [GetProtocolFromTable](getprotocolfromtable.md) 函數。

</dd> <dt>

*lpInstData* \[in、out\]
</dt> <dd>

在輸入上，從先前的通訊協定指向實例資料的指標。

在輸出時，為目前通訊協定的實例資料指標。 實例資料的長度不能超過 DWORD \_ 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是已辨識之剖析器資料之後第一個位元組的指標。 如果剖析器宣告所有剩餘的資料，則傳回值為 **Null**。

如果函式不成功，則傳回值是 *lpProtocol* 參數傳入的初始指標。

## <a name="remarks"></a>備註

**RecognizeFrame** 函式會判斷剖析器是否從 *lpProtocol* 指標開始識別原始資料。

-   如果通訊協定辨識資料， **RecognizeFrame** 函式會傳回剩餘資料的指標，如果目前的通訊協定是框架中的最後一個通訊協定，則會傳回 **Null** 。
-   如果通訊協定無法辨識資料， **RecognizeFrame** 函式會傳回在 *lpProtocol* 參數中傳遞至剖析器 DLL 的指標。

> [!Note]  
> 您可以在呼叫 [*register*](register-parser.md)函數之前呼叫 *RecognizeFrame* ，以註冊通訊協定屬性。 基於這個理由， *RecognizeFrame* 函式的執行不依賴在通訊協定 **註冊** 函式執行期間所建立或初始化的任何屬性或結構。

 

**交付集和後續設定**

剖析器可以使用「認可集」或「設定」（set）來識別網路監視器遵循辨識資料的通訊協定。

-   如果可辨識的資料中有可用的資訊，剖析器會使用它的遞交集來取得下一個通訊協定的控制碼，然後將該控制碼傳遞給網路監視器。
-   如果資訊無法使用，剖析器不會傳遞控制碼，網路監視器會使用剖析器之後的設定來決定接下來的通訊協定。

**在通訊協定之間傳遞資訊**

使用 *lpInstData* 參數傳遞通訊協定之間的資訊。 在輸入上，您可以從先前的通訊協定取得資訊。 在輸出中，您可以將資訊傳遞至下一個通訊協定。

實例資料可以是小於或等於 DWORD 指標長度的任何資料，或是不需要由剖析器配置 \_ 或釋放的資料指標，例如原始框架資料。



| 的相關資訊                                        | 請參閱                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。 | [解析 器](parsers.md)                                                                                                    |
| 剖析器 DLL 中包含的進入點。        | [剖析器 DLL 架構](parser-dll-architecture.md)                                                                    |
| 如何執行 **RecognizeFrame**  包含範例。 | [執行 RecognizeFrame](implementing-recognizeframe.md)                                                            |
| 如何指定遞交集，並遵循 set。              | [指定追蹤集](specifying-a-handoff-set.md)[指定追蹤](specifying-a-follow-set.md)集<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> </dl>

 

 




