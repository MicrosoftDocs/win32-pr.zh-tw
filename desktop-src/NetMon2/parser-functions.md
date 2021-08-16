---
description: 剖析器會呼叫下列 helper 函數。
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: 剖析器函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d70c3ad44ad809a323af8acde732af3b142759d3686d78c496f47e92cb8e209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676838"
---
# <a name="parser-functions"></a>剖析器函式

剖析器會呼叫下列 helper 函數。



| 函式                                                 | 描述                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [AddressToString](addresstostring.md)                   | 將位址轉換成字串。                                                                               |
| [LookupByteSetString](lookupbytesetstring.md)           | 抓取對應至已加上標籤集合之指定值的字串。                                    |
| [SetCCInstPtr](setccinstptr.md)                         | 捕捉內容實例指標。                                                                           |
| [StringToAddress](stringtoaddress.md)                   | 將字串轉換成位址。                                                                               |
| [VarLenSmallIntToDword](varlensmallinttodword.md)       | 將可變長度、小整數轉換成 **DWORD**。                                                      |
| [LookupDwordSetString](lookupdwordsetstring.md)         | 抓取對應至已加上標籤集合之指定值的字串。                                    |
| [LookupWordSetString](lookupwordsetstring.md)           | 從加上標籤的集合中，抓取對應至指定值的字串。                                      |
| [BERGetHeader](bergetheader.md)                         | 解碼選擇標頭。                                                                                       |
| [BERGetInteger](bergetinteger.md)                       | 解碼 BER 編碼的整數。                                                                                 |
| [BERGetString](bergetstring.md)                         | 將 BER 編碼的字串解碼。                                                                                  |
| [CCHeapAlloc](ccheapalloc.md)                           | 依捕捉逐一配置記憶體。                                                                |
| [CCHeapFree](ccheapfree.md)                             | 釋放 **CCHeapAlloc** 函式所配置的記憶體。                                                 |
| [CCHeapReAlloc](ccheaprealloc.md)                       | 重新配置 **CCHeapAlloc** 函式所配置的記憶體。                                                  |
| [CCHeapSize](ccheapsize.md)                             | 捕獲 **CCHeapAlloc** 函式所配置的記憶體大小。                                    |
| [GetCCInstPtr](getccinstptr.md)                         | 抓取已新增至 capture 內容之實例資料的指標。                                       |
| [CreateProtocol](createprotocol.md)                     | 通知網路監視器 API 存在特定的通訊協定剖析器。                                        |
| [DestroyProtocol](destroyprotocol.md)                   | 終結 **CreateProtocol** 函數所建立的通訊協定。                                              |
| [BuildINIPath](buildinipath.md)                         | 抓取與您輸入的資訊對應的初始化 (INI) 檔案的完整路徑。   |
| [CreateHandoffTable](createhandofftable.md)             | 根據指定的 INI 檔案中的資訊建立遞交資料表。                                             |
| [DestroyHandoffTable](destroyhandofftable.md)           | 終結使用 **CreateHandoffTable** 函式建立的交付資料表。                                     |
| [GetProtocolFromTable](getprotocolfromtable.md)         | 抓取指定之遞交資料表的通訊協定。                                                               |
| [AddProperty](/previous-versions/bb251873(v=msdn.10))                           | 將 **PROPERTYINFO** 結構加入至屬性資料庫。                                                    |
| [AttachPropertyInstance](attachpropertyinstance.md)     | 將屬性實例附加至框架。                                                                       |
| [AttachPropertyInstanceEx](attachpropertyinstanceex.md) | 將屬性實例附加至框架。                                                                       |
| [CreatePropertyDatabase](createpropertydatabase.md)     | 建立描述剖析器用來描述其資料之屬性的屬性資料庫。               |
| [DestroyPropertyDatabase](destroypropertydatabase.md)   | 終結呼叫 **CreatePropertyDatabase** 和 **AddProperty** 函數所建立的屬性資料庫。 |
| [FindNextFrame](findnextframe.md)                       | 在目前的捕獲內容中尋找符合指定篩選的下一個畫面格。                               |
| [FindPreviousFrame](findpreviousframe.md)               | 在目前的捕獲內容中尋找符合指定篩選準則的先前框架。                           |
| [FormatPropertyInstance](formatpropertyinstance.md)     | 以一般方式格式化屬性實例。                                                             |
| [GetFrameDestAddress](getframedestaddress.md)           | 抓取框架的目的位址。                                                                  |
| [GetFrameSourceAddress](getframesourceaddress.md)       | 抓取框架的來源位址。                                                                       |
| [GetProtocolStartOffset](getprotocolstartoffset.md)     | 抓取框架中指定之通訊協定的位移。                                                         |
| [ParserTemporaryLockFrame](parsertemporarylockframe.md) | 當框架進入剖析器時鎖定框架，並在框架結束時將其解除鎖定。                                     |



 

如需匯出函式的詳細資訊 (可由專家和剖析器呼叫的 helper 函式) 、結構和列舉，請參閱下列主題。



| 如需下列資訊                                  | 請參閱                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| 剖析器匯出的函式。                         | [剖析器 DLL 匯出函數](parser-dll-export-functions.md)               |
| 剖析器函數使用的結構。                  | [剖析器結構](parser-structures.md)                                   |
| 剖析器和專家呼叫的一般協助程式函式。 | [專家和剖析器一般函數](expert-and-parser-common-functions.md) |



 

 

 
