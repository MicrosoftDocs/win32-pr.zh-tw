---
title: CGENOBJ.Cpp
description: 在範例提供者元件中，在 cgenobj 中支援的泛型 Active Directory 物件方法，如下表所示。
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe769dcfa6e4ab607188728115bcba16e40c0e56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671179"
---
# <a name="cgenobjcpp"></a>CGENOBJ.Cpp

在範例提供者元件中，在 cgenobj 中支援的泛型 Active Directory 物件方法，如下表所示。



| 方法                                                                                  | 描述                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObject::CSampleDSGenObject**                                              | 標準的函式。                                                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject：： ~ CSampleDSGenObject**                                             | 標準的函式。                                                                                                                                                                                                                                                                                                        |
| **CSampleDSGenObject::CreateGenericObject**                                             | 建立 ADS 泛型物件。 視需要初始化。                                                                                                                                                                                                                                                                    |
| **CSampleDSGenObject::SampleDSCreateObject**                                            | 在其父容器中建立此物件。                                                                                                                                                                                                                                                                                 |
| **CSampleDSGenObject::SampleDSSetObject**                                               | 儲存此物件的屬性 (清除快取) 。                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::AllocateGenObject**                                               | 建立泛型物件並載入其類型資料。                                                                                                                                                                                                                                                                             |
| **CSampleDSGenObject：： QueryInterface**                                                  | 傳回要求的介面指標（如果有的話）。                                                                                                                                                                                                                                                                       |
| 標準 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 方法，包括下列各方面的：                   | [**取得**](/windows/desktop/api/Iads/nf-iads-iads-get) (包括從原生資料類型到 variant 類型的對應) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) (包括從 VARIANT 類型到原生資料類型的對應) <br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (重新整理屬性快取) <br/> [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) (儲存屬性快取) <br/> |
| 標準 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 方法，包括下列各方面的： | [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**取得 \_ 篩選**](iadscontainer-property-methods.md)<br/> [**建立**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**刪除**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **ConvertSafeArrayToVariantArray**                                                      | 公用程式常式。                                                                                                                                                                                                                                                                                                            |



 

 

 





