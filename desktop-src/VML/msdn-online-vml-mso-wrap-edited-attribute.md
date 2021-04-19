---
title: VML MSO-自動換行編輯的屬性
description: VML MSO-自動換行編輯的屬性
ms.assetid: cb0e8618-e649-4a3c-9433-2be77c4b65f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a272a56b57d82ca0fee9f69fbde2757316439fd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969911"
---
# <a name="vml-mso-wrap-edited-attribute"></a>VML MSO-自動換行編輯的屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷換行座標是否由使用者自訂。 讀取/寫入 **VgTriState**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* style = "mso-wrap-已編輯： *expression* " >

**備註**

如果自動換行座標是由編輯器所產生，則這個屬性為 **True**;否則會由使用者自訂。

*Microsoft Office Extensions 屬性*

**範例**

圖形的換行座標是由圖形編輯器所產生。


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-edited:True"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 