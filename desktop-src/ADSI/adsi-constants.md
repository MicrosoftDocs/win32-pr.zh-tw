---
title: ADSI 常數
description: 下表列出 Active Directory 服務介面中定義和使用的常數 (ADSI) 。
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671191"
---
# <a name="adsi-constants"></a>ADSI 常數

下表列出 Active Directory 服務介面中定義和使用的常數 (ADSI) 。



| ADSI 常數                      | 值                                   | 描述                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ EXT \_ INITCREDENTIALS**      | 1                                       | 代表提供給 [**IADsExtension：：操作**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) 方法的自訂資料包含使用者認證的控制項程式碼。                                                     |
| **ADS \_ EXT \_ INITIALIZE \_ 完成** | 2                                       | 搭配 [**IADsExtension：：操作**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) 所使用的控制項程式碼，指出延伸模組可以執行任何必要的初始化，端視父物件所支援的功能而定。 |
| **ADS \_ EXT \_ MAXEXTDISPID**         | 16777215                                | 擴充物件可用於其方法和屬性的 DISPID 最高。                                                                                                                                   |
| **ADS \_ EXT \_ MINEXTDISPID**         | 1                                       | 擴充物件可用於其方法和屬性的最小 DISPID。                                                                                                                                    |
| **ADS \_ VLV \_ 回應**             | L "fc8cb04d-311d-406c-8cb9-1ae8b843b419" | 搭配 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 方法使用，以取得 VLV 搜尋中繼資料。 如需詳細資訊，請參閱 [如何使用 VLV 搜尋](how-to-search-using-vlv.md)。        |
| **DBPROPFLAGS \_ ADSISEARCH**        | 0x0000C000                              | 用來處理 OLE DB 提供者。                                                                                                                                                                           |



 

 

 




