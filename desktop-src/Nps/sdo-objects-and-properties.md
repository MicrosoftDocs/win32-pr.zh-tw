---
title: 物件與屬性
description: 在 SDO 中，物件的特性取決於物件的屬性，以及與這些屬性相關聯的值。
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967907"
---
# <a name="objects-and-properties"></a>物件與屬性

在 SDO 中，物件的特性取決於物件的屬性，以及與這些屬性相關聯的值。 不同于其他的物件模型，SDO 物件本身沒有方法。 不過，SDO 物件確實會公開提供方法的 COM 介面。

SDO 中的物件會公開 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) 介面，以提供處理物件屬性的方法。 若要存取物件的屬性，請取得物件的 **ISdo** 介面，並使用 [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) 和 [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) 介面方法來取得和設定屬性的值。 抓取 [使用者 SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) 的主題包含範例程式碼，示範如何取得使用者物件的 **ISdo** 介面。

對物件的屬性進行變更之後，請使用 [**ISdo：： Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) 方法，將變更寫入至物件的持續性儲存區。 您可以藉由呼叫 [**ISdo：： Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore)方法，在呼叫 **ISdo：： Apply** 之前，取消對物件屬性所做的變更。 這個方法會從持續性儲存體還原物件屬性的值。

下表顯示列舉 SDO 中某些物件屬性的列舉類型。



| Object                                 | 列舉類型                                       |
|----------------------------------------|--------------------------------------------------------|
| 所有 SDO 物件                        | [**IASCOMMONPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| User 物件                            | [**USERPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
|  (網路原則伺服器的服務物件)  | [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| Microsoft RADIUS 通訊協定物件       | [**RADIUSPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。

 

## <a name="collections"></a>集合

物件通常群組為集合。 SDO API 透過 [**ISdo 集合**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) 介面提供功能，以列舉集合中的物件，以及加入和刪除集合中的物件。

取得集合的存取權的方法是在包含集合的物件上取得集合屬性。 如需詳細資訊，請參閱 [物件模型](/windows/desktop/Nps/sdo-object-model-hierarchy)階層中的一節。

所有對應至集合之屬性的資料類型都是 VT \_ 分派。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SDO 物件模型階層](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[SDO 支援的屬性](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 