---
description: Assert 和中斷點宏
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Assert 和中斷點宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109733"
---
# <a name="assert-and-breakpoint-macros"></a>Assert 和中斷點宏

[DirectShow 基類](directshow-base-classes.md)提供數個執行判斷提示或導致中斷點的宏。



| 巨集                                        | Description                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**斷言**](assert.md)                     | 評估運算式，並在運算式為 **FALSE** 時顯示診斷訊息。                                         |
| [**DbgAssertAligned**](dbgassertaligned.md) | 測試指標是否對齊指定的界限。                                                                        |
| [**DbgBreak**](dbgbreak.md)                 | 使用指定的字串、來源檔案的名稱和行號，顯示訊息方塊。                                |
| [**EXECUTE \_ ASSERT**](execute-assert.md)    | 評估 debug 和 retail 組建中的運算式。 在 [偵錯工具] 組建中，如果運算式為 **FALSE**，則會顯示診斷訊息。 |
| [**KASSERT**](kassert.md)                   | 評估運算式，並在運算式為 **FALSE** 時引發中斷點例外狀況。                                         |
| [**KDbgBreak**](kdbgbreak.md)               | 導致中斷點例外狀況，並記錄指定的字串。                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[偵錯工具](debugging-utilities.md)
</dt> </dl>

 

 



