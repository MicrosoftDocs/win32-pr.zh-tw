---
title: 使用 IDirectoryObject 介面
description: 當您在 C 或 c + + 中建立使用早期繫結的 ADSI 用戶端時，如果您的用戶端呼叫 IDirectoryObject 介面，而不是 IADs 介面，您將會有更多的 ADSI 資料類型可供使用。
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- 使用 IDirectoryObject ADSI
- ADSI ADSI，使用 IDirectoryObject 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671104"
---
# <a name="using-the-idirectoryobject-interface"></a>使用 IDirectoryObject 介面

當您在 C 或 c + + 中建立使用早期繫結的 ADSI 用戶端時，如果您的用戶端呼叫 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面，而不是 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面，您將會有更多的 adsi 資料類型可供使用。 **IDirectoryObject** 介面提供的方法可支援物件的維護屬性子集，以及存取其屬性。 下圖顯示資料結構之間的關聯性。

![idirectoryobject 介面資料結構](images/ds2dso.png)

在上圖中，structure [**ADS \_ 物件 \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_object_info) 定義的屬性會依分辨名稱、相對分辨名稱、容器 (p n) 、依物件類型 (ClassDN) ，以及架構定義 (SchemaDN) 來識別物件。 屬性描述項 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)包含名稱、資料類型、 [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)中所顯示的資料值陣列，以及指示基礎目錄服務對 [ADS \_ ATTR \_ \*](adsi-constants.md)屬性中詳細說明的屬性執行特定作業的旗標。 這些屬性的資料類型包括 ADSI 擴充語法類型，如 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)中所述。

 

 




