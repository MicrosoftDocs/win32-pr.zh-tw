---
description: Direct3D 10 set 函數不會保存裝置子物件的參考。
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: " (Direct3D 10) 的參考計數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335452"
---
# <a name="reference-counting-direct3d-10"></a> (Direct3D 10) 的參考計數

Direct3D 10 set 函數不會保存裝置子物件的參考。 這表示，只要物件需要系結至管線，每個應用程式都必須保存裝置子物件的參考。 當物件的參考計數降至零時，該物件就會從管線解除系結並終結。 這種參考的樣式也稱為弱式參考，因為每個管線系結位置都持有與其系結之介面/物件的弱式參考。

例如︰


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





Direct3D 9 與 Direct3D 10 之間的差異：

- 在 Direct3D 9 中，set 函數會保存裝置物件的參考;在 Direct3D 10 中，set 函數不會保存裝置子物件的參考。



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的 API 功能 ](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




