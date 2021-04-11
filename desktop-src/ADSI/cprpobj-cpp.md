---
title: CPRPOBJ.Cpp
description: 在範例提供者元件中，屬性物件方法（在 cprpobj 中）會列在下表中。
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182994"
---
# <a name="cprpobjcpp"></a>CPRPOBJ.Cpp

在範例提供者元件中，屬性物件方法（在 cprpobj 中）會列在下表中。



| 方法                                                 | 描述                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSProperty::CSampleDSProperty**               | 標準的函式。                                                                                                                          |
| **CSampleDSProperty：： ~ CSampleDSProperty**              | 標準的函式。                                                                                                                           |
| **CSampleDSProperty：： CreateProperty**                  | 建立 ADS 屬性物件，藉由呼叫 **SampleDSGetPropertyDefinition** 來查閱屬性定義。                              |
| **CSampleDSProperty：： CreateProperty**                  | 在指定屬性定義的情況下，建立屬性物件，並設定支援的 ADS 語法與提供者語法之間的對應。 |
| **CSampleDSProperty::AllocatePropertyObject**          | 建立屬性物件並載入其類型資料。                                                                                               |
| **CSampleDSProperty：： QueryInterface**                  | 傳回要求的介面指標（如果有的話）。                                                                                          |
| 標準 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 方法。                 |                                                                                                                                                |
| 標準 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) 方法。 |                                                                                                                                                |
| **MapSyntaxIdtoADsSyntax**                             | 設定語法識別碼和 ADS 語法之間的對應。                                                                               |
| **MapSyntaxIdtoSampleDSSyntax**                        | 設定語法識別碼與提供者語法之間的對應。                                                                          |



 

 

 




