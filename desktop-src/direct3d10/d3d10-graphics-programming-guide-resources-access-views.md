---
description: 在 Direct3D 10 中，材質資源是使用 view 來存取，這是在記憶體中資源的硬體轉譯機制。
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: " (Direct3D 10) 的材質視圖"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc420e39c4d577947cae657f3296b15f0052db9e823e07d3a3ba1ccb641fb6b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101339"
---
# <a name="texture-views-direct3d-10"></a> (Direct3D 10) 的材質視圖

在 Direct3D 10 中，材質資源是使用 view 來存取，這是在記憶體中資源的硬體轉譯機制。 檢視允許特定的管線階段，在應用程式所要的表示中，只能存取其所需的[子資源](d3d10-graphics-programming-guide-resources-types.md)。

視圖支援無類型資源的概念。 不具類型的資源是以特定大小建立的資源，但不是特定資料類型。 資料在與管線繫結之後會進行動態解譯。

下列圖例呈現了透過建立著色器資源檢視，以將 2D 紋理陣列與 6 個紋理繫結，作為著色器資源使用的範例。 資源接著便會作為紋理陣列進行定址。 (注意︰子資源無法同時作為輸入及輸出繫結。)

![六個紋理的紋理陣列圖例](images/d3d10-cube-texture-faces.png)

當使用 2D 紋理陣列作為轉譯目標時，資源可以作為具備 Mipmap 層級 (在此範例中為 3) 的 2D 紋理陣列 (在此範例中為 6 個紋理) 檢視。

透過呼叫 CreateRenderTargetView 以建立轉譯目標的檢視物件。 接著呼叫 OMSetRenderTargets 為管線設定轉譯目標檢視。 藉由呼叫 Draw 及使用 RenderTargetArrayIndex，索引至陣列中適當的紋理，並且轉譯進轉譯目標之中。 您可使用子資源 (一個 Mipmap 層級與陣列索引的組合) 繫結至任何子資源的陣列。 如此一來，您就可以繫結至第二個 Mipmap 層級，並且在您需要的時候只更新此一特定 Mipmap 層級，如下圖例所示。

![僅繫結至紋理陣列的第二個 Mipmap 層級之圖例](images/d3d10-cube-texture-faces-subresource.png)



Direct3D 9 與 Direct3D 10 之間的差異：

- 在 Direct3D 10 中，您不再將資源直接系結至管線、建立資源的視圖，然後將視圖設定為管線。 這可讓執行時間和驅動程式中的驗證和對應發生于建立時，並在系結時將類型檢查降至最低。



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




