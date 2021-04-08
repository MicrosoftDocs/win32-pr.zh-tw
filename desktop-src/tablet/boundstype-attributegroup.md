---
description: 定義日誌 XML 檔案中各種專案所使用的屬性群組。 它包含屬性，用來定義檔中專案的左邊、頂端、高度和寬度)  (範圍。
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: BoundsType 屬性群組
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689231"
---
# <a name="boundstype-attribute-group"></a>BoundsType 屬性群組

定義日誌 XML 檔案中各種專案所使用的屬性群組。 它包含屬性，用來定義檔中專案的左邊、頂端、高度和寬度)  (範圍。

## <a name="definition"></a>定義

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a>子元素

無。

## <a name="attributes"></a>屬性



| 屬性  | 類型                      | 必要 | 描述                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **離開**   | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最左邊點的距離。<br/> | 任何整數。<br/>              |
| **前幾個**    | **xs:integer**            | 必要 | 從原點到專案之周框方塊中最上方點的距離。<br/>  | 任何整數。<br/>              |
| **寬度**  | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的寬度。<br/>                                          | 任何非負整數。<br/> |
| **高度** | **xs:nonNegativeInteger** | 必要 | 元素周框方塊的高度。<br/>                                         | 任何非負整數。<br/> |



 

## <a name="type-information"></a>類型資訊



|             |                                            |
|-------------|--------------------------------------------|
| 命名空間   | urn：架構-microsoft-com：平板電腦： richink |
| 結構描述名稱 | 日誌讀者                             |



 

## <a name="remarks"></a>備註

**左邊** 和 **頂端** 可以是負數，因為來源是由邊界（而非頁面）所定義。

 

 




