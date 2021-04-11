---
description: 這些值會搭配 ImmGetConversionStatus 和 ImmSetConversionStatus 函數使用。
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: IME 轉換模式值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113624"
---
# <a name="ime-conversion-mode-values"></a>IME 轉換模式值

這些值會搭配 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 和 [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) 函數使用。



| bit                      | 意義                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| IME \_ CMODE 英 \_ 數位元 | 英數位元輸入模式。 這是預設值，定義為0x0000。                          |
| IME \_ CMODE \_ CHARCODE     | 如果字元碼輸入模式，則設定為 1;如果沒有，則為0。                                          |
| 輸入法 \_ CMODE \_ EUDC         | 如果 EUDC 轉換模式，則設定為 1;如果沒有，則為0。                                               |
| 輸入法 \_ CMODE \_ 固定        | **Windows Me/98、windows 2000、WINDOWS XP：** 如果固定的轉換模式，則設定為 1;如果沒有，則為0。 |
| IME \_ CMODE \_ FULLSHAPE    | 如果全圖形模式，則設定為 1;如果為半形狀模式，則為0。                                        |
| IME \_ CMODE \_ HANJACONVERT | 如果是漢字轉換模式，則設定為 1;如果沒有，則為0。                                                 |
| 輸入法 \_ CMODE \_ 片假名     | 若為片假名模式，則設定為 1;若為平假名模式，則為0。                                            |
| IME \_ CMODE \_ 原生       | 如果原生模式，則設定為 1;若為英數位元模式，則為0。                                          |
| IME \_ CMODE \_ NOCONVERSION | 設定為1以防止依 IME 處理轉換;如果沒有，則為0。                           |
| IME \_ CMODE \_ 羅馬        | 如果羅馬字輸入模式，則設定為 1;如果沒有，則為0。                                                   |
| IME \_ CMODE \_ SOFTKBD      | 如果軟鍵盤模式，則設定為 1;如果沒有，則為0。                                                 |
| IME \_ CMODE \_ 符號       | 如果符號轉換模式，則設定為 1;如果沒有，則為0。                                             |



 

所有其他位都是保留的。

 

 



