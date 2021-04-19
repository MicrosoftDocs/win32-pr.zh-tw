---
description: 下表所列的網路監視器函式，可用來開發剖析器或專家。
ms.assetid: 26eb4f99-a8dc-43a2-abb9-9577518b6f2f
title: 專家和剖析器一般函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6776260610c2decb0ecf91b6373d301937d899b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973421"
---
# <a name="expert-and-parser-common-functions"></a>專家和剖析器一般函數

下表所列的網路監視器函式，可用來開發剖析 [*器或*](p.md)[*專家*](e.md)。



| 函式                                                               | 描述                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [CompareAddresses](compareaddresses.md)                               | 比較兩個指定的位址。                                                       |
| [CompareFrameDestAddress](compareframedestaddress.md)                 | 比較指定的位址與框架的目的位址。                     |
| [CompareFrameSourceAddress](compareframesourceaddress.md)             | 比較指定位址與框架的來源位址。                          |
| [FilterAddObject](filteraddobject.md)                                 | 將單一物件新增至篩選準則。                                                   |
| [FindPropertyInstance](findpropertyinstance.md)                       | 尋找指定屬性的第一個實例。                                       |
| [FindPropertyInstanceRestart](findpropertyinstancerestart.md)         | 尋找指定屬性的下一個實例。                                        |
| [GetCaptureComment](getcapturecomment.md)                             | 抓取捕捉的批註。                                                 |
| [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)     | 從其 capture 檔案抓取 capture 的批註。                           |
| [GetCaptureMacType](getcapturemactype.md)                             | 抓取 capture 的 MAC 型別。                                              |
| [GetCaptureTimeStamp](getcapturetimestamp.md)                         | 抓取 capture timeout 戳記。                                                |
| [GetCaptureTotalFrames](getcapturetotalframes.md)                     | 抓取捕捉中的總畫面格。                                          |
| [GetEnabledProtocols](getenabledprotocols.md)                         | 抓取所有標示為已啟用的通訊協定清單。                            |
| [GetFrame](getframe.md)                                               | 抓取指定框架的控制碼。                                                |
| [GetFrameCaptureHandle](getframecapturehandle.md)                     | 抓取指定之捕捉的控制碼。                                              |
| [GetFrameDstAddressOffset](getframedstaddressoffset.md)               | 抓取指定框架的目的地位址位移。                         |
| [GetFrameFromFrameHandle](getframefromframehandle.md)                 | 抓取指定框架控點的框架。                                         |
| [GetFrameLength](getframelength.md)                                   | 抓取指定框架的長度。                                              |
| [GetFrameMacHeaderLength](getframemacheaderlength.md)                 | 抓取指定框架的 MAC 標頭長度。                           |
| [GetFrameMacType](getframemactype.md)                                 | 抓取指定框架的 MAC 型別。                                           |
| [GetFrameNumber](getframenumber.md)                                   | 傳回指定框架的編號。                                                |
| [GetFrameRecognizeData](getframerecognizedata.md)                     | 抓取通訊協定識別碼 (以及其在所有辨識的通訊協定) 的位移。 |
| [GetFrameSrcAddressOffset](getframesrcaddressoffset.md)               | 抓取給定框架的來源位址位移。                        |
| [GetFrameStoredLength](getframestoredlength.md)                       | 抓取指定框架的長度。                                              |
| [GetFrameTimeStamp](getframetimestamp.md)                             | 抓取指定框架的時間戳記。                                          |
| [GetPreviousProtocolOffsetByName](getpreviousprotocoloffsetbyname.md) | 抓取指定通訊協定的上一個實例。                                |
| [GetProperty](getproperty.md)                                         | 抓取具有指定名稱的屬性。                                             |
| [GetPropertyInfo](getpropertyinfo.md)                                 | 抓取特定屬性的資訊。                                   |
| [GetPropertyText](getpropertytext.md)                                 | 抓取指定屬性的文字。                                             |
| [GetProtocolFromName](getprotocolfromname.md)                         | 依名稱抓取特定的通訊協定。                                              |
| [GetProtocolInfo](getprotocolinfo.md)                                 | 使用通訊協定控制碼來抓取與通訊協定相關的資料。                        |
| [GetProtocolStartOffsetHandle](getprotocolstartoffsethandle.md)       | 抓取指定通訊協定的位移。                                           |
| [MacTypeToAddressType](mactypetoaddresstype.md)                       | 將 MAC 類型轉換為網址類別型。                                             |
| [ModifyFrame](modifyframe.md)                                         | 以新資料更新現有的框架。                                            |



 

如需專家所使用的函式和結構的詳細資訊，以及剖析器僅使用的函式和結構的詳細資訊，請參閱下表所列的主題。



| 如需下列項目的詳細資訊                                          | 請參閱                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| 您可以用來開發專家 Dll 的專家專屬功能。 | [專家功能、結構和列舉](expert-functions-structures-and-enumerations.md) |
| 您可以用來開發剖析器 Dll 的剖析器專用函數。 | [剖析器函式和結構](parser-functions-and-structures.md)                             |



 

 

 



