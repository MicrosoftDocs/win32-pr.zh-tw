---
title: VML ShapeType 元素
description: VML ShapeType 元素
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186000"
---
# <a name="vml-shapetype-element"></a>VML ShapeType 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義可以用來建立其他圖形的圖形。

下列屬性會修改 **ShapeType**。



| 屬性                                      | 描述                                             |
|------------------------------------------------|---------------------------------------------------------|
| [主機](msdn-online-vml-master-attribute.md) | 判斷 **ShapeType** 是否為主要元素。 |



 

**備註**

**ShapeType** 與 **Shape** 元素相同，不同之處在于它無法參考另一個 **ShapeType** 元素。

當 **shape** 元素參考 **ShapeType** 時， **圖形** 可能會複製已在 **ShapeType** 中指定的部分屬性。 在這些情況下， **圖形** 中的屬性會覆寫 **ShapeType** 的屬性。

**Type** 屬性不得與 **ShapeType** 搭配使用。

CSS 定位屬性 (例如 **頂端**、**左方** 等 ) 不會從 **ShapeType** 傳遞給 **圖形**。

若要使用這個元素，請建立具有特定 [識別碼](id-attribute--vml.md)屬性的 **ShapeType** 。 然後建立一個 **圖形**，並以 **Type** 屬性參考 **ShapeType** 。 如需詳細資訊，請參閱 [Type](type-attribute--shape--vml.md) 屬性。

 

 