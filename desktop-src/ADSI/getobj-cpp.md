---
title: GETOBJ.Cpp
description: 在 [範例提供者] 元件中，會顯示用來尋找和系結物件的程式碼範例位於 Getobj .cpp 中。 下表列出支援的常式。
ms.assetid: d202e5ec-27b5-4809-a7fa-4a2e39c65295
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d58647208c68437c068d58cd9908bc08989141
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316462"
---
# <a name="getobjcpp"></a>GETOBJ.Cpp

在 [範例提供者] 元件中，會顯示用來尋找和系結物件的程式碼範例位於 Getobj .cpp 中。 下表列出支援的常式。



| 項目                                | 描述                                                                                                                                                                                                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RelativeGetObject**               | 取得相對於指定 ADsPath 的物件。                                                                                                                                                                                                                                                       |
| **GetObject**                       | 呼叫 **ADsObject** (Parse) 以驗證路徑語法，驗證路徑是否具有正確的提供者 token，並驗證物件類型。 如果沒有錯誤存在，請建立正確類型之物件的實例，並取得物件 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面的指標。 |
| **BuildADsPathFromDSPath**          | 從原生目錄路徑建立 ADsPath 字串。                                                                                                                                                                                                                                           |
| **BuildDSTreeNameFromADsPath**      | 使用 ADsPath 為原生目錄路徑建立可能的樹狀目錄路徑。                                                                                                                                                                                                           |
| **BuildDSPathFromADsPath**          | 使用 ADsPath 和 DSPathName。                                                                                                                                                                                                                                                                      |
| **BuildADsParentPath**              | 將 ADsPath 建立至這個物件的父系。                                                                                                                                                                                                                                                  |
| **GetNamespaceObject**              | 驗證和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 範例命名空間物件。                                                                                                                                                                                                           |
| **ValidateNamespaceObject**         | 確認 namespace 物件符合目前的提供者名稱。                                                                                                                                                                                                                               |
| **ValidateProvider**                | 驗證提供者名稱 (區分大小寫的) 。                                                                                                                                                                                                                                                          |
| **GetSchemaObject**                 | 驗證並開啟適當的架構物件類型。 然後建立正確的檔案，並在其上取出 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。                                                                                                                                        |
| **ValidateSchemaObject**            | 確認它是有效的架構物件類型。                                                                                                                                                                                                                                                     |
| **ValidateObjectType**              | 確認物件類型存在於架構中。                                                                                                                                                                                                                                                 |
| **BuildSampleDSRootRDNFromADsPath** | 建立 ADsPath 至範例提供者元件的根節點。                                                                                                                                                                                                                            |
| **BuildDSPathFromADsPath**          | 使用 ADsPath、DSRootRDN 和 DSPathName。                                                                                                                                                                                                                                                          |



 

 

 