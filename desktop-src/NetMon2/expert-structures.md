---
description: 網路監視器和一般 helper 函式所提供的專家協助程式函式會使用下表所述的結構。
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: 專家結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16accf769b0983b782a6e6dbd723dd08df27415220bda1d59122b951439bac65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939015"
---
# <a name="expert-structures"></a>專家結構

網路監視器和一般 helper 函式所提供的專家協助程式函式會使用下表所述的結構。



| 結構                                              | Description                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**CONFIGUREDEXPERT**](configuredexpert.md)           | 將專家 DLL 與其設定產生關聯。                                                       |
| [**EXPERTCONFIG**](expertconfig.md)                   | 提供原始的設定資料。                                                                       |
| [**EXPERTENUMINFO**](expertenuminfo.md)               | 提供專家 DLL 的相關資訊。 網路監視器會使用資訊。                       |
| [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) | 提供框架的相關資訊。                                                                    |
| [**EXPERTSTARTUPINFO**](expertstartupinfo.md)         | 提供專家的相關啟動資訊。                                                         |
| [**EXPERTSTATUS**](expertstatus.md)                   | 提供正在執行之專家的目前狀態。                                                       |
| [**FILTEROBJECT**](filterobject.md)                   | 定義專家的顯示篩選特性。                                              |
| [**NMEVENTDATA**](nmeventdata.md)                     | 提供專家檢視器中顯示的行相關資訊。                                      |
| [**NMCOLUMNINFO**](nmcolumninfo.md)                   | 提供在事件檢視器中定義資料行的資訊。                                        |
| [**NMCOLUMNVARIANT**](nmcolumnvariant.md)             | 提供容器，讓所有可能的資料插入事件檢視器中一行的資料行。     |
| [**NMCOLUMNTYPE**](nmcolumntype.md)                   | 變數中的進入點，指出要使用聯集的哪個元素，以及如何將它格式化。 |



 

網路監視器也提供 (helper 函式的匯出函式，專家可以呼叫) 和列舉。



| 如需下列資訊                                          | 請參閱                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| 匯出函式，將進入點提供給您的專家 DLL。 | [專家 DLL 匯出函式](expert-dll-export-functions.md)               |
| 可由專家和剖析器呼叫的 Helper 函式。    | [專家和剖析器一般函數](expert-and-parser-common-functions.md) |
| 僅由專家呼叫的 Helper 函式。              | [專家功能](expert-functions.md)                                     |
| 專家結構和函數所使用的列舉。          | [專家列舉](expert-enumerations.md)                               |



 

 

 



