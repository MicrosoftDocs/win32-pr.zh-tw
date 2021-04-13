---
title: REGDSAPI.Cpp
description: 在範例提供者元件中，代表直接存取原生作業系統之 API 的函式位於 Regdsapi .cpp 中。
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e160ab212960753c6f793f734ebd96dffdd0f9e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300067"
---
# <a name="regdsapicpp"></a>REGDSAPI.Cpp

在範例提供者元件中，代表直接存取原生作業系統之 API 的函式位於 Regdsapi .cpp 中。 範例提供者元件會在登錄中執行其目錄服務。 若要撰寫可存取您自己目錄服務的提供者，請建立您自己的此 API 的實作為。 下表列出支援的功能。



| 方法                             | 描述                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SampleDSOpenObject**             | 依名稱開啟此物件。 如果架構類別型別參數為 **Null**，請填入找到的類型。 取得物件的控制碼。                                                             |
| **SampleDSCloseObject**            | 使用 **SampleDSOpenObject** 取出的控制碼。                                                                                                                                            |
| **SampleDSRDNEnum**                | 取得列舉值物件的控制碼，以管理從容器物件 (RDNs) 的相對辨別名稱列舉。                                                          |
| **SampleDSNextRDN**                | 使用 **SampleDSRDNEnum** 抓取的控制碼，從這個容器物件取得下一個相對分辨名稱。                                                                        |
| **SampleDSFreeEnum**               | 釋放在 **SampleDSRDNEnum** 中配置的列舉值物件。                                                                                                                                   |
| **SampleDSModifyObject**           | 修改目錄服務中物件的屬性，並指定物件的控制碼，以及屬性及其值的清單。                                                              |
| **SampleDSReadObject**             | 從目錄服務讀取物件的屬性。 將原生儲存的語法對應至適當的 ADS 語法值。 據以處理多個值的屬性。 |
| **SampleDSGetPropertyDefinition**  | 在架構中，針對此類型的架構類別物件，查閱所有屬性定義和其屬性。                                                                                     |
| **SampleDSGetPropertyDefinition**  | 在架構中，依名稱查閱此屬性和其屬性。                                                                                                                               |
| **SampleDSFreePropertyDefinition** | **GetPropertyDefinition** 所配置的可用記憶體。                                                                                                                                            |
| **SampleDSGetTypeText**            | 以文字格式取得物件的架構類別類型。                                                                                                                                         |
| **SampleDSGetType**                | 取得物件的架構類別型別。                                                                                                                                                        |
| **SampleDSGetPropertyInfo**        | 在架構類別物件和屬性名稱上提供控制碼，以抓取屬性資訊，例如語法等等。                                                                      |
| **FreeList**                       | 釋放 LPWSTR 清單所使用的記憶體 \_ 。                                                                                                                                                        |
| **SampleDSGetClassDefinition**     | 從架構中取出所有架構類別定義和其相關資料的集合。                                                                                                    |
| **SampleDSGetClassDefinition**     | 取得架構中特定架構類別的相關資料。                                                                                                                                   |
| **SampleDSGetClassInfo**           | 指定架構類別的名稱，查詢其相關聯的資料，例如強制屬性。                                                                                                      |
| **SampleDSAddObject**              | 在目錄服務中新增物件。                                                                                                                                                        |
| **SampleDSRemoveObject**           | 從目錄服務移除物件。                                                                                                                                                   |
| **SampleDSCreateBuffer**           | 建立屬性資料和作業資料的記憶體緩衝區。                                                                                                                                  |
| **SampleDSFreeBuffer**             | 釋放在 **SampleDSCreateBuffer** 中建立的緩衝區。                                                                                                                                           |



 

 

 




