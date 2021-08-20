---
title: 'Src 屬性 (VMLFrame)  (VML) '
description: 'Src 屬性 (VMLFrame)  (VML) '
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f7761a55304eefc655d00ed58d84b7af8f7ce5daf86a3aaf462308b43c193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057579"
---
# <a name="src-attribute-vmlframevml"></a>Src 屬性 (VMLFrame)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義框架的資料來源。 讀取/寫入 **字串**。

**適用於**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**標記語法**

<v： *element* src = " *expression* " >

**指令碼語法**

 src = "*expression*"

*運算式* =*元素* src

**備註**

**Src** 屬性可能包含下列語法：

-   外部檔案的 URL。 檔案必須是具有下列格式的 XML 檔案：
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   在檔案中，您必須有一個或多個具有有效識別碼的 VML 圖形，而且可以使用此語法來參考：
    ```HTML
       filename#shapename
    ```

    

-   在下列參考中，外部檔案的副檔名為 vml，但可以使用任何擴充功能：
    ```HTML
       external.vml#image01
    ```

    

-   您可以使用下列語法，在相同檔案中參考圖形：
    ```HTML
       #shapename
    ```

    

如果 **剪輯** 為 **False**，圖形將會縮放以符合框架。 若 **為 True**，將不會顯示框架外之圖形的任何部分。

請注意，除非 **剪輯** 為 **True**，否則不會使用 [原始](origin-attribute--vmlframe--vml.md)和 [大小](size-attribute--vmlframe.md)。

**VML 標準屬性**

**範例**

外部檔案中定義的映射將會被裁剪。


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 