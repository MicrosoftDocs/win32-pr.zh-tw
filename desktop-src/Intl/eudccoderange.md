---
description: EUDCCodeRange 登錄機碼會針對 (字元集) 的各種字碼頁，定義使用者定義的字元 (EUDC) 程式碼範圍。
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120673"
---
# <a name="eudccoderange"></a>EUDCCodeRange

EUDCCodeRange 登錄機碼會針對 (字元集) 的各種字碼頁，定義 [使用者定義的字元 (EUDC) ](end-user-defined-characters.md) 程式碼範圍。 它僅供建立 EUDCs 的工具使用，而不是對 EUDC 使用者的直接關注。 此登錄機碼具有下列登錄位置：

HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ 字碼頁 \\ EUDCCodeRange

其格式為：

EUDCCodeRange 字碼頁 = FromTo \[ 、FromTo\]

其中：



| 值         | 描述                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | 其中一個字串 "932" (日文) 、"936" (簡體中文) 、"949" (韓文) 、"950" (繁體中文) 或 "Unicode" (Unicode) 。 不支援其他值。                                     |
| FromTo   | 由一組4位數的十六進位值所組成的字串值，以連字號 ( ) 。 最多可以指定四個 FromTo 值，但每個值都必須以逗號分隔， (，) 。 |



 

以下是登錄專案的正確值。


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[EUDC 登錄專案](eudc-registry-entries.md)
</dt> <dt>

[EUDC](eudc.md)
</dt> </dl>

 

 



