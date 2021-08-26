---
description: 剖析器 DLL 的架構必須提供下圖所示的功能。
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: 剖析器 DLL 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b2c3ead77d5172bc57fa3bc1c8b6001b9c690cd254dc436ac93f504ddb732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962860"
---
# <a name="parser-dll-architecture"></a>剖析器 DLL 架構

剖析器 DLL 的架構必須提供下圖所示的功能。 請注意，某些功能只需要執行一個進入點。 但是，如果您的剖析器 DLL 支援多個通訊協定，則功能需要執行多個進入點。

![剖析器 dll 功能](images/parserarchitecture1.png)



| 如需下列資訊                                                  | 請參閱                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| 如何執行剖析器 DLL 匯出函數。                          | [撰寫通訊協定剖析器](writing-a-protocol-parser.md)             |
| 剖析器使用的特定函式和結構—參考主題。 | [剖析器函式和結構](parser-functions-and-structures.md) |



 

 

 



