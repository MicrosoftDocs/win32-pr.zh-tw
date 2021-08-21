---
title: CENUMSCH.CPP
description: 在範例提供者元件中，架構物件的列舉會使用下表所列 cenumsch 中的方法。
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b9be8a58f2d3775f11f85f590f374fc67902a73891484c57e5756645390fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840518"
---
# <a name="cenumschcpp"></a>CENUMSCH.CPP

在範例提供者元件中，架構物件的列舉會使用下表所列 cenumsch 中的方法。



| 方法                                        | 描述                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **CSampleDSSchemaEnum：： Create**               | 建立物件以允許 ADSI 架構類別物件的列舉。                                                |
| **CSampleDSSchemaEnum::CSampleDSSchemaEnum**  | 標準的函式。                                                                                                |
| **CSampleDSSchemaEnum：： ~ CSampleDSSchemaEnum** | 標準的函式。                                                                                                 |
| **CSampleDSSchemaEnum：： Next**                 | 從指定的架構物件中取出指定的元素數目。                                          |
| **CSampleDSSchemaEnum：： EnumObjects**          | 管理如何抓取介面指標，指向所指定物件類型的物件。                               |
| **CSampleDSSchemaEnum：： EnumObjects**          | 管理如何抓取預設物件類型之物件的介面指標。                                  |
| **CSampleDSSchemaEnum::EnumClasses**          | 管理只抓取此物件中包含之架構類別物件的介面指標。                  |
| **CSampleDSSchemaEnum：： GetClassObject**       | 取出下一個架構類別定義;如果找到，請建立架構類別物件，並傳回介面指標。 |
| **CSampleDSSchemaEnum：： EnumProperties**       | 管理將介面指標僅包含在此物件中的屬性物件。                      |
| **CSampleDSSchemaEnum::GetPropertyObject**    | 取出下一個屬性定義;如果找到，請建立架構類別物件，並傳回介面指標。     |
| **CSampleDSSchemaEnum::EnumSyntaxes**         | 管理將介面指標僅包含在此物件中的介面物件。                        |
| **CSampleDSSchemaEnum::GetSyntaxObject**      | 取出下一個語法定義;如果找到，請建立架構類別物件，並傳回介面指標。       |



 

 

 




