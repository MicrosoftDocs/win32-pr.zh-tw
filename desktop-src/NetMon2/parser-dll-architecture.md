---
description: 剖析器 DLL 的架構必須提供下圖所示的功能。
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: 剖析器 DLL 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469513"
---
# <a name="parser-dll-architecture"></a>剖析器 DLL 架構

剖析器 DLL 的架構必須提供下圖所示的功能。 請注意，某些功能只需要執行一個進入點。 但是，如果您的剖析器 DLL 支援多個通訊協定，則功能需要執行多個進入點。

![剖析器 dll 功能](images/parserarchitecture1.png)



| 如需下列資訊                                                  | 請參閱                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| 如何執行剖析器 DLL 匯出函數。                          | [撰寫通訊協定剖析器](writing-a-protocol-parser.md)             |
| 剖析器使用的特定函式和結構—參考主題。 | [剖析器函式和結構](parser-functions-and-structures.md) |



 

 

 



