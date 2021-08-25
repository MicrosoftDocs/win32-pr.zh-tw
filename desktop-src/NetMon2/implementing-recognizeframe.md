---
description: 網路監視器會呼叫剖析器的 RecognizeFrame 函式，以判斷剖析器是否能辨識框架的取消認領資料。
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: 執行 RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d3f9a79325c0c75a7a83cfb99a34ff3de1f073573dee13d39a846b575f6285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890491"
---
# <a name="implementing-recognizeframe"></a>執行 RecognizeFrame

網路監視器會呼叫剖析器的 [**RecognizeFrame**](recognizeframe.md) 函式，以判斷剖析器是否能辨識框架的取消認領資料。 取消認領資料可能位於框架的開頭，但是取消認領資料通常位於框架的中間。 下圖顯示位於框架中間的取消認領資料。

![取消認領位於框架中間的資料](images/recognizeframe1.png)

網路監視器在呼叫 [**RecognizeFrame**](recognizeframe.md) 函數時提供下列資訊：

-   框架的控制碼。
-   框架開頭的指標。
-   取消認領資料開頭的指標。
-   框架中第一個通訊協定的 MAC 值。
-   取消認領資料中的位元組數目;也就是框架中剩餘的位元組。
-   先前通訊協定的控制碼。
-   先前通訊協定的位移。

當剖析器 DLL 判斷取消認領資料是從剖析器通訊協定開始時，剖析器 DLL 會決定下一個通訊協定的開始位置，以及接下來的通訊協定。 剖析器 DLL 會以下列條件方式運作：

-   如果剖析器 DLL 辨識取消認領資料，剖析器 DLL 會設定 *pProtocolStatus* 參數，並將指標傳回至框架中的下一個通訊協定，或傳回 **Null**。 如果目前的通訊協定是框架中的最後一個通訊協定，則會傳回 **Null** 。
-   如果剖析器 DLL 辨識出取消認領的資料，並從通訊協定) 所提供的資訊 (識別接下來的通訊協定，則剖析器 DLL 會將指標傳回至函式之 *phNextProtocol* 參數中下一個通訊協定的控制碼。
-   如果剖析器 DLL 無法辨識取消認領資料，剖析器 DLL 會傳回取消認領資料開頭的指標，網路監視器繼續嘗試剖析取消認領資料。

**若要執行 RecognizeFrame**

1.  測試以判斷您是否辨識了通訊協定。
2.  如果您辨識取消認領資料，並知道接下來的通訊協定，請將 *pProtocolStatus* 設定為 [通訊協定 \_ 狀態 \_ 下一個 \_ 通訊協定]，將 *phNextProtocol* 設定為指向下一個通訊協定控制碼的指標，然後將指標傳回至下一個通訊協定。

    –或–

    如果您辨識取消認領資料，但不知道接下來的通訊協定，請將 *pProtocolStatus* 設定為 [辨識的通訊協定 \_ 狀態 \_ ]，然後將指標傳回至下一個通訊協定。

    –或–

    如果您辨識取消認領資料，而您的通訊協定是框架中的最後一個通訊協定，請將 *pProtocolStatus* 設定為已宣告的通訊協定 \_ 狀態，然後傳回 \_ **Null**。

    –或–

    如果您無法辨識取消認領資料，請將 *pProtocolStatus* 設定為無法辨識的通訊協定 \_ 狀態 \_ \_ ，然後傳回在 *pProtocol* 中傳遞給您的指標。

以下是 [**RecognizeFrame**](recognizeframe.md)的基本執行。

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



