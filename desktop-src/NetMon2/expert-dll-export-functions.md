---
description: 下列功能是專家 Dll 的進入點，以及作業系統和網路監視器的呼叫。
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: 專家 DLL 匯出函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327b36990ac377595b31b55ebc0ed57157fd8d411f690aff3378293f35e39e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911128"
---
# <a name="expert-dll-export-functions"></a>專家 DLL 匯出函式

下列功能是專家 Dll 的進入點，以及作業系統和網路監視器的呼叫。



| 函式                                   | 描述                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DllMain 專家**](dllmain-expert.md)   | 表示已載入或卸載專家 DLL。 當進程載入或卸載 DLL 時，作業系統會呼叫 [**DllMain**](/windows/desktop/Dlls/dllmain) 函數。 |
| [**註冊專家**](register-expert.md) | 判斷有關 DLL 內專家的基本資訊。 網路監視器會呼叫 **Register** 函數。                                                           |
| [**設定**](configure.md)             | 設定 DLL 內的專家。 網路監視器會呼叫 [**Configure**](configure.md) 函數。                                                                 |
| [**執行**](run.md)                         | 啟動 DLL 內的專家。 網路監視器會呼叫 [**Run**](run.md) 函數。                                                                                 |



 

網路監視器也提供專家可以呼叫的結構、列舉和 helper 函式。



| 如需下列資訊                                      | 請參閱                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| 可由專家和剖析器呼叫的協助程式函數 | [專家和剖析器一般函數](expert-and-parser-common-functions.md) |
| 僅由專家呼叫的 Helper 函式           | [專家功能](expert-functions.md)                                     |
| 專家函式所使用的結構               | [專家結構](expert-structures.md)                                   |
| 專家結構和函數所使用的列舉       | [專家列舉](expert-enumerations.md)                               |



 

 

 
