---
title: 如何編制多個輸出資料流程的索引
description: 在著色器模型5中，幾何著色器最多可以支援4個不同的資料流程。 這表示單一著色器可以在一到四個輸出資料流程之間輸出，視宣告的資料流程數目而定。
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020921"
---
# <a name="how-to-index-multiple-output-streams"></a>如何：編制多個輸出資料流程的索引

在著色器模型5中，幾何著色器最多可以支援4個不同的資料流程。 這表示單一著色器可以在一到四個輸出資料流程之間輸出，視宣告的資料流程數目而定。

編制多個輸出資料流程的索引

1.  使用資料流程範本類型來定義資料流程。

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  使用資料流程範本類型定義第二個數據流。

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  使用資料流程輸出物件內部 (函數（例如 Append 或 RestartStrip) ）將資料輸出到 (或兩者) 資料流程。

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

使用單一輸出資料流程時，您可以發出三角形的條紋、行條紋或點清單。 當您在資料流程輸出緩衝區中儲存三角形和帶狀線時，它們會分別展開為三角形和線條清單。 您也可以將一個資料流程柵格化，而不將它傳送至記憶體緩衝區。

使用多個輸出資料流程時，所有的資料流程都必須包含點，而最多可將一個輸出資料流程傳送至轉譯器。 更常見的情況是，應用程式不會將任何資料流程柵格化。

將資料串流至緩衝區之後，您可以使用該資料來轉譯任何基本類型，而不只是用來填滿緩衝區的基本型別。

幾何著色器的輸出總計限制為1024個純量。 當有多個資料流程存在時，會從最大的資料流程類型乘以最大頂點計數來計算純量數目。



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>著色器模型4和著色器模型5之間的差異：<br/> 著色器模型4：<br/>
<ul>
<li>資料流程輸出的純量最大數目是64。</li>
<li>每個元件的暫存器遮罩必須在索引範圍內相符。</li>
</ul>
著色器模型5：<br/>
<ul>
<li>資料流程輸出的純量最大數目是128。</li>
<li>每個元件的暫存器遮罩不需要在索引範圍內相符。</li>
<li>輸出的動態索引在所有串流之間必須是合法的。</li>
<li>插補模式不需要與資料流程相符。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[幾何著色器功能](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





