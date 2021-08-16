---
description: 以下是離線登錄庫功能。
ms.assetid: 378811d2-064c-4d81-979e-392097d55baa
title: 離線登錄庫函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400aeddf652948fac135b73b0512d157d17b1d71e83b5a5399c5c34618872323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826706"
---
# <a name="offline-registry-library-functions"></a>離線登錄庫函數

以下是離線登錄庫功能。



| 函式                                       | 描述                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**ORCloseHive**](orclosehive.md)             | 關閉指定的離線登錄 hive，並釋出配置給 hive 的記憶體。                                 |
| [**ORCloseKey**](orclosekey.md)               | 關閉離線登錄 hive 中指定之登錄機碼的控制碼。                                          |
| [**ORCreateHive**](orcreatehive.md)           | 建立包含單一空根金鑰的離線登錄 hive。                                             |
| [**ORCreateKey**](orcreatekey.md)             | 在離線登錄 hive 中建立指定的登錄機碼。 如果索引鍵已經存在，則函式會將它開啟。   |
| [**ORDeleteKey**](ordeletekey.md)             | 從離線登錄 hive 刪除子機碼及其值。                                                      |
| [**ORDeleteValue**](ordeletevalue.md)         | 從離線登錄 hive 中的指定登錄機碼移除值。                                        |
| [**OREnumKey**](orenumkey.md)                 | 列舉離線登錄 hive 中指定之開啟登錄機碼的子機碼。                              |
| [**OREnumValue**](orenumvalue.md)             | 列舉離線登錄區中指定之開啟登錄機碼的值。                              |
| [**ORGetKeySecurity**](orgetkeysecurity.md)   | 抓取保護離線登錄區中指定之開啟登錄機碼的安全描述項複本。 |
| [**ORGetValue**](orgetvalue.md)               | 抓取離線登錄 hive 中指定之登錄值的類型和資料。                           |
| [**ORGetVersion**](orgetversion.md)           | 捕獲離線登錄庫的版本。                                                              |
| [**ORGetVirtualFlags**](orgetvirtualflags.md) | 抓取離線登錄區中指定的開啟登錄機碼上的虛擬旗標。                         |
| [**OROpenHive**](oropenhive.md)               | 將指定的 hive 檔案載入記憶體中，並驗證 hive。                                                   |
| [**OROpenKey**](oropenkey.md)                 | 在離線登錄 hive 中開啟指定的登錄機碼。                                                       |
| [**ORQueryInfoKey**](orqueryinfokey.md)       | 抓取離線登錄 hive 中指定之登錄機碼的相關資訊。                                 |
| [**ORSaveHive**](orsavehive.md)               | 將指定的離線登錄 hive 寫入檔案。                                                               |
| [**ORSetKeySecurity**](orsetkeysecurity.md)   | 設定離線登錄區中已開啟登錄機碼的安全性。                                              |
| [**ORSetValue**](orsetvalue.md)               | 設定離線登錄區中所指定登錄機碼值的資料。                                |
| [**ORSetVirtualFlags**](orsetvirtualflags.md) | 在離線登錄區中，于指定的開啟登錄機碼上設定虛擬旗標。                           |



 

 

 



