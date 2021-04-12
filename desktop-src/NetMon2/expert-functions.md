---
description: 下列 helper 函式只能由匯出執行或設定函數的專家呼叫。
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: 專家功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847745"
---
# <a name="expert-functions"></a>專家功能

下列 helper 函式只能由匯出 [執行](run.md) 或 [設定](configure.md) 函數的專家呼叫。



| 函式                                         | 描述                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ExpertGetFrame](expertgetframe.md)             | 從捕捉中取出指定的框架。                                               |
| [ExpertIndicateStatus](expertindicatestatus.md) | 指出專家的「capture」分析完成的百分比。             |
| [ExpertGetStartupInfo](expertgetstartupinfo.md) | 抓取專家的啟動資訊。                                       |
| [ExpertMemorySize](expertmemorysize.md)         | 抓取 **ExpertAllocMemory** 函式的呼叫所配置的記憶體大小。 |
| [ExpertSubmitEvent](expertsubmitevent.md)       | 指出問題，並抓取問題的相關資訊（如果有的話）。          |
| [ExpertAllocMemory](expertallocmemory.md)       | 配置專家的記憶體。                                                        |
| [ExpertReallocMemory](expertreallocmemory.md)   | 變更 **ExpertAllocMemory** 函式所配置的記憶體大小。         |
| [ExpertFreeMemory](expertfreememory.md)         | 釋出專家所配置的記憶體。                                                   |



 

如需匯出函式、專家和剖析器、結構和列舉可呼叫的 helper 函式的詳細資訊，請參閱下列主題：



| 如需下列資訊                                             | 請參閱                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| 由專家匯出的功能                            | [專家 DLL 匯出函式](expert-dll-export-functions.md)               |
| 專家函式所使用的結構                      | [專家結構](expert-structures.md)                                   |
| 專家結構和函數所使用的列舉              | [專家列舉](expert-enumerations.md)                               |
| 專家和剖析器可呼叫的一般協助程式函式 | [專家和剖析器一般函數](expert-and-parser-common-functions.md) |



 

 

 



