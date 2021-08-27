---
description: 下表所列的函式是剖析器 Dll 的進入點。 這些函式是從作業系統和網路監視器呼叫的進入點。
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: 剖析器 DLL 匯出函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c04eb57cf5d5f76b60bca43fc5ed47ae641182efc74b21c8b41fa5d909af6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037028"
---
# <a name="parser-dll-export-functions"></a>剖析器 DLL 匯出函數

下表所列的函式是剖析器 Dll 的進入點。 這些函式是從作業系統和網路監視器呼叫的進入點。



| 函式                                           | 描述                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllMain 剖析器](dllmain-parser.md)               | 指示剖析器 DLL 載入或卸載它。 當進程載入或卸載 DLL 時，作業系統會呼叫 **DllMain** 剖析器函式。 |
| [AttachProperties](attachproperties.md)           | 通知剖析器附加存在於框架中的任何屬性。                                                                                            |
| [取消註冊](deregister.md)                       | 通知剖析器清除。                                                                                                                               |
| [FormatProperties](formatproperties.md)           | 通知剖析器取得中的所有屬性實例，並建立每個 **PROPERTYINST** 結構的 **szPropertyText** 成員。                       |
| [RecognizeFrame](recognizeframe.md)               | 判斷剖析器是否可以使用指定的通訊協定來解讀未處理的框架資料。                                                            |
| [註冊剖析器](register-parser.md)             | 判斷 DLL 內剖析器的基本資訊。 網路監視器會呼叫 **Register** 剖析器函數。                                          |
| [ParserAutoInstallInfo](parserautoinstallinfo.md) | 自動安裝剖析器。                                                                                                                               |



 

網路監視器提供剖析器可呼叫的結構和 helper 函數。



| 如需下列項目的詳細資訊                          | 請參閱                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| 專家和剖析器可以呼叫的協助程式函數。 | [專家和剖析器一般函數](expert-and-parser-common-functions.md) |
| 只有剖析器可以呼叫的 Helper 函數。        | [剖析器函式](parser-functions.md)                                     |
| 剖析器函數使用的結構。               | [剖析器結構](parser-structures.md)                                   |



 

 

 



