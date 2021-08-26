---
description: 本章節描述您可以用來開發剖析器的結構。 您可以用來開發剖析器和功能的函式會使用這些結構來開發剖析器或專家。
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: 剖析器結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d54e02e26e9874f27f49312a84b4b643cc4b3bfdb0c6056f274e4febecf0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082528"
---
# <a name="parser-structures"></a>剖析器結構

本章節描述您可以用來開發剖析器的結構。 您可以用來開發剖析器和功能的函式會使用這些結構來開發剖析器或專家。



| 結構                                 | 描述                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MACFRAME](macframe.md)                  | 定義最常使用的初始通訊協定。                                                                               |
| [E](entrypoints.md)            | 指定剖析器 DLL 進入點的指標。                                                                      |
| [PF \_ FOLLOWENTRY](pf-followentry.md)     | 指定遵循目前通訊協定的通訊協定。                                                                       |
| [PF \_ FOLLOWSET](pf-followset.md)         | 指定遵循目前通訊協定的通訊協定組。                                                               |
| [PF \_ HANDOFFENTRY](pf-handoffentry.md)   | 指定將通訊協定交給目前的通訊協定，或目前的通訊協定所用的通訊協定。    |
| [PF \_ HANDOFFSET](pf-handoffset.md)       | 指定一組送出目前通訊協定的通訊協定，或目前通訊協定所要關閉的通訊協定組。 |
| [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) | 指定剖析器 DLL 中的剖析器數目和每個剖析器的相關資訊。                                            |
| [PF \_ PARSERINFO](pf-parserinfo.md)       | 指定特定剖析器的相關資訊。                                                                                  |
| [標示為 \_ 位](labeled-bit.md)           | 指定控制碼、位欄位或旗標。                                                                                        |
| [標記的 \_ 位元組](labeled-byte.md)         | 指定 **位元組** 標籤組。                                                                                                |
| [標記的 \_ DWORD](labeled-dword.md)       | 指定 **DWORD** 標籤組。                                                                                               |
| [標示為 \_ WORD](labeled-word.md)         | 指定 **單字** 標籤組。                                                                                                |
| [PROPERTYINFO](propertyinfo.md)          | 指定通訊協定剖析器所需的屬性來描述畫面格。                                                  |
| [PROPERTYINST](propertyinst.md)          | 指定框架中屬性的實例。                                                                                 |
| [PROPERTYINSTEX](propertyinstex.md)      | 指定自由格式的擴充屬性實例。                                                                              |
| [PROTOCOLINFO](protocolinfo.md)          | 指定通訊協定。                                                                                                           |
| [範圍](range.md)                        | 指定數位的範圍。                                                                                                 |
| [SET](set.md)                            | 指定屬性值的資料表。                                                                                     |



 

如需用於開發剖析器 Dll 之函數的詳細資訊，請參閱下列主題。



| 如需下列資訊                                         | 請參閱                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| 剖析器 Dll 匯出的函式。                        | [剖析器 DLL 匯出函數](parser-dll-export-functions.md)               |
| 您可以用來開發剖析器 Dll 的函式。            | [剖析器函式](parser-functions.md)                                     |
| 您可以用來開發剖析器和專家 Dll 的函式。 | [專家和剖析器一般函數](expert-and-parser-common-functions.md) |



 

 

 



