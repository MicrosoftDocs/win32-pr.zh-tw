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
# <a name="how-to-index-multiple-output-streams"></a><span data-ttu-id="30e3e-104">如何：編制多個輸出資料流程的索引</span><span class="sxs-lookup"><span data-stu-id="30e3e-104">How To: Index Multiple Output Streams</span></span>

<span data-ttu-id="30e3e-105">在著色器模型5中，幾何著色器最多可以支援4個不同的資料流程。</span><span class="sxs-lookup"><span data-stu-id="30e3e-105">In shader model 5, a geometry shader can support up to 4 separate streams.</span></span> <span data-ttu-id="30e3e-106">這表示單一著色器可以在一到四個輸出資料流程之間輸出，視宣告的資料流程數目而定。</span><span class="sxs-lookup"><span data-stu-id="30e3e-106">This means a single shader can output between one and four output streams, depending on the number of streams declared.</span></span>

<span data-ttu-id="30e3e-107">編制多個輸出資料流程的索引</span><span class="sxs-lookup"><span data-stu-id="30e3e-107">To index multiple output streams</span></span>

1.  <span data-ttu-id="30e3e-108">使用資料流程範本類型來定義資料流程。</span><span class="sxs-lookup"><span data-stu-id="30e3e-108">Define a data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  <span data-ttu-id="30e3e-109">使用資料流程範本類型定義第二個數據流。</span><span class="sxs-lookup"><span data-stu-id="30e3e-109">Define a second data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  <span data-ttu-id="30e3e-110">使用資料流程輸出物件內部 (函數（例如 Append 或 RestartStrip) ）將資料輸出到 (或兩者) 資料流程。</span><span class="sxs-lookup"><span data-stu-id="30e3e-110">Output data to either (or both) streams using the stream output object intrinsic functions (such as Append or RestartStrip).</span></span>

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

    

<span data-ttu-id="30e3e-111">使用單一輸出資料流程時，您可以發出三角形的條紋、行條紋或點清單。</span><span class="sxs-lookup"><span data-stu-id="30e3e-111">When using a single output stream, you can emit triangle strips, line strips, or point lists.</span></span> <span data-ttu-id="30e3e-112">當您在資料流程輸出緩衝區中儲存三角形和帶狀線時，它們會分別展開為三角形和線條清單。</span><span class="sxs-lookup"><span data-stu-id="30e3e-112">When you store triangle and line strips in the stream out buffer, they are expanded to triangle and line lists respectively.</span></span> <span data-ttu-id="30e3e-113">您也可以將一個資料流程柵格化，而不將它傳送至記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="30e3e-113">You can also rasterize one stream and not send it to a memory buffer.</span></span>

<span data-ttu-id="30e3e-114">使用多個輸出資料流程時，所有的資料流程都必須包含點，而最多可將一個輸出資料流程傳送至轉譯器。</span><span class="sxs-lookup"><span data-stu-id="30e3e-114">When using multiple output streams, all streams must contain points, and up to one output stream can be sent to the rasterizer.</span></span> <span data-ttu-id="30e3e-115">更常見的情況是，應用程式不會將任何資料流程柵格化。</span><span class="sxs-lookup"><span data-stu-id="30e3e-115">More commonly, an application will not rasterize any stream.</span></span>

<span data-ttu-id="30e3e-116">將資料串流至緩衝區之後，您可以使用該資料來轉譯任何基本類型，而不只是用來填滿緩衝區的基本型別。</span><span class="sxs-lookup"><span data-stu-id="30e3e-116">After you stream data to a buffer, you can use that data to render any primitive type, not just the primitive type that you used to fill the buffer.</span></span>

<span data-ttu-id="30e3e-117">幾何著色器的輸出總計限制為1024個純量。</span><span class="sxs-lookup"><span data-stu-id="30e3e-117">The total output of the geometry shader is limited to 1024 scalars.</span></span> <span data-ttu-id="30e3e-118">當有多個資料流程存在時，會從最大的資料流程類型乘以最大頂點計數來計算純量數目。</span><span class="sxs-lookup"><span data-stu-id="30e3e-118">When multiple streams exist, the number of scalars is computed from the largest stream type multiplied by the maximum vertex count.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30e3e-119">著色器模型4和著色器模型5之間的差異：</span><span class="sxs-lookup"><span data-stu-id="30e3e-119">Differences between shader model 4 and shader model 5:</span></span><br/> <span data-ttu-id="30e3e-120">著色器模型4：</span><span class="sxs-lookup"><span data-stu-id="30e3e-120">Shader model 4:</span></span><br/>
<ul>
<li><span data-ttu-id="30e3e-121">資料流程輸出的純量最大數目是64。</span><span class="sxs-lookup"><span data-stu-id="30e3e-121">Maximum number of scalars for stream output is 64.</span></span></li>
<li><span data-ttu-id="30e3e-122">每個元件的暫存器遮罩必須在索引範圍內相符。</span><span class="sxs-lookup"><span data-stu-id="30e3e-122">The per-component register mask must match across the index range.</span></span></li>
</ul>
<span data-ttu-id="30e3e-123">著色器模型5：</span><span class="sxs-lookup"><span data-stu-id="30e3e-123">Shader model 5:</span></span><br/>
<ul>
<li><span data-ttu-id="30e3e-124">資料流程輸出的純量最大數目是128。</span><span class="sxs-lookup"><span data-stu-id="30e3e-124">Maximum number of scalars for stream output is 128.</span></span></li>
<li><span data-ttu-id="30e3e-125">每個元件的暫存器遮罩不需要在索引範圍內相符。</span><span class="sxs-lookup"><span data-stu-id="30e3e-125">The per-component register mask does not need to match across the index range.</span></span></li>
<li><span data-ttu-id="30e3e-126">輸出的動態索引在所有串流之間必須是合法的。</span><span class="sxs-lookup"><span data-stu-id="30e3e-126">Dynamic indexing of outputs must be legal across all streams.</span></span></li>
<li><span data-ttu-id="30e3e-127">插補模式不需要與資料流程相符。</span><span class="sxs-lookup"><span data-stu-id="30e3e-127">Interpolation modes do not need to match for the streams.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="30e3e-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="30e3e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e3e-129">幾何著色器功能</span><span class="sxs-lookup"><span data-stu-id="30e3e-129">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





