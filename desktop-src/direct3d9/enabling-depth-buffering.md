---
description: 當您建立深度緩衝區（如建立深度緩衝區 (Direct3D 9) 所述）之後，您可以藉由呼叫 IDirect3DDevice9：： Graphicsdevice 方法來啟用深度緩衝。
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: " (Direct3D 9) 啟用深度緩衝"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317547"
---
# <a name="enabling-depth-buffering-direct3d-9"></a> (Direct3D 9) 啟用深度緩衝

當您建立深度緩衝區（如 [建立深度緩衝區 (Direct3D 9)](creating-a-depth-buffer.md)所述）之後，您可以藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/desktop/api) 方法來啟用深度緩衝。 設定 D3DRS \_ ZENABLE 轉譯狀態以啟用深度緩衝。 使用 \_ [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) 列舉型別的 D3DZB TRUE 成員 (或 **TRUE**) 來啟用 z 緩衝、D3DZB \_ USEW 來啟用 w-緩衝或 D3DZB \_ false (或 **false**) 停用深度緩衝。

> [!Note]  
> 若要使用 w 緩衝，您的應用程式必須設定符合規範的投射矩陣，即使它不使用 Direct3D 轉換管線也一樣。 如需有關提供適當投射矩陣的詳細資訊，請參閱 [W 易記投射矩陣](projection-transform.md)

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[深度緩衝區](depth-buffers.md)
</dt> </dl>

 

 
