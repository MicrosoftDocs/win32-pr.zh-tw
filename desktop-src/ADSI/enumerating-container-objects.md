---
title: 列舉容器物件
description: 依照慣例，ADSI 中列舉的所有專案都必須是相同的 Automation 資料類型。 例如，列舉不應將某些專案傳回為 VT I4 型別的變數 \_ ，而其他專案則為 vt BSTR 類型的變異 \_ 。
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968820"
---
# <a name="enumerating-container-objects"></a>列舉容器物件

依照慣例，ADSI 中列舉的所有專案都必須是相同的 Automation 資料類型。 例如，列舉不應將某些專案傳回為 **vt \_ I4** 型別的 **變數**，而其他專案則為 **vt \_ BSTR** 類型的 **變異**。

為了列舉物件所維護的專案清單，用戶端會要求針對所列出的特定資訊類型建立列舉物件。 在 ADSI 中，用戶端可能會列出命名空間物件、泛型容器物件、集合物件、成員物件或架構物件中的物件。 ADSI 提供的篩選準則可以設定和修改，以限制任何列舉中的相符專案，但 [**IADsContainer. filter**](iadscontainer-property-methods.md) 屬性。 您可以在下列 ADs 容器物件的範例提供者元件程式碼中找到列舉值物件的範例。



| 物件型別         | code         |
|---------------------|--------------|
| 一般容器   | cenumobj .cpp |
| 命名空間容器 | cenumns .cpp  |
| 架構容器    | cenumsch .cpp |



 

如需用戶端資訊，請參閱 [集合和群組](collections-and-groups.md)。

 

 




