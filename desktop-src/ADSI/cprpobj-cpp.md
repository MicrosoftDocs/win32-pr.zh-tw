---
title: CPRPOBJ.CPP
description: 在範例提供者元件中，屬性物件方法（在 cprpobj 中）會列在下表中。
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb130d6deced939aa718e839c0e7f178329e6a5b14c383dbf1a2719c0f25cfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840332"
---
# <a name="cprpobjcpp"></a>CPRPOBJ.CPP

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



 

 

 




