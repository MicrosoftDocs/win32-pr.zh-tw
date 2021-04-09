---
description: 網路監視器提供 PROPERTYINFO 結構來定義通訊協定的屬性，以及 PROPERTYINST 和 PROPERTYINSTEX 結構來定義屬性的實例。
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: 屬性定義和屬性實例結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692783"
---
# <a name="property-definition-and-property-instance-structures"></a>屬性定義和屬性實例結構

網路監視器提供 [**PROPERTYINFO**](propertyinfo.md) 結構來定義通訊協定的屬性，以及 [**PROPERTYINST**](propertyinst.md)和 [**PROPERTYINSTEX**](propertyinstex.md) 結構來定義屬性的實例。

![網路監視器結構](images/property1.png)

剖析器會為通訊協定支援的所有屬性配置和填入 [**PROPERTYINFO**](propertyinfo.md) 結構。 剖析器會將結構傳遞給網路監視器，其中結構會新增至通訊協定 [*屬性資料庫*](p.md)。 當剖析屬性的實例，以及將網路監視器 UI 中顯示的資料格式化時，會使用 **PROPERTYINFO** 結構中的資訊。

當剖析器將屬性定義附加至屬性的實例時，網路監視器會配置 [**PROPERTYINST**](propertyinst.md) 和 [**PROPERTYINSTEX**](propertyinstex.md) 結構。

下列程式識別附加屬性定義所需的步驟。

**附加屬性定義**

1.  識別存在於通訊協定實例中的每個屬性。 附加定義時，網路監視器會將捕獲的資料傳遞給剖析器。 資料會根據通訊協定實例來傳遞。
2.  判斷通訊協定實例中屬性的位置。
3.  將屬性定義附加至屬性位置。

當剖析器使用存在於捕捉中的屬性資料時，網路監視器會執行 [**PROPERTYINST**](propertyinst.md) 結構。 當剖析器必須修改 capture 中的屬性資料時，網路監視器會執行 [**PROPERTYINSTEX**](propertyinstex.md) 結構。

 

 



