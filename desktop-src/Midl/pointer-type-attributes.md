---
title: 指標類型屬性
description: 下列屬性會指定指標的特性。
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL MIDL、屬性、指標類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675771"
---
# <a name="pointer-type-attributes"></a>指標類型屬性

下列屬性會指定指標的特性。



| 屬性                                   | 使用方式                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ptr**](ptr.md)                          | 使用 C 語言指標的所有功能（包括別名）將指標指定為完整指標。                                                                                       |
| [**ref**](ref.md)                          | 指定 MIDL 中最簡單的指標類型，一個只提供某些資料的位址。 參考指標永遠不可以是 null。                                                             |
| [**獨特**](unique.md)                    | 讓指標為 null，但不支援別名。                                                                                                                                               |
| [**指標 \_ 預設值**](pointer-default.md) | 套用至介面，以指定該介面中所有指標的預設指標類型，但最上層參數指標除外，後者會自動預設為 [**ref**](ref.md) 指標。 |
| [**iid \_ 為**](iid-is.md)                   | 提供 COM 介面的介面識別碼，該介面是指標的物件。                                                                                                            |
| [**字串**](string.md)                    | 指定指標指向字串。                                                                                                                                                       |



 

 

 




