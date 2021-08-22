---
title: 呼叫-vs
description: 對以提供的標籤標記的指令執行函式呼叫。 |呼叫-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2321224b10ca1f7822b19e48ebbb58c1e01c261720f64a8b39331fbceab75fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986888"
---
# <a name="call---vs"></a>呼叫-vs

對以提供的標籤標記的指令執行函式呼叫。

## <a name="syntax"></a>Syntax



| 呼叫 l\# |
|----------|



 

其中 l \# 是 [標籤-vs](label---vs.md) 標示要呼叫的副程式開頭。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| call                   |      | x    | x    | x     | x    | x     |



 

此指令會執行下列動作：

1.  將下一個指令推送至傳回位址堆疊的位址。
2.  從標籤標記的指令繼續執行。

在頂點著色器 2 \_ 0 中，不允許使用嵌套呼叫。

在頂點著色器 2 \_ x 中，嵌套深度會受限於 [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) 結構的 StaticFlowControlDepth 元素。 如需詳細資訊，請參閱 [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps)。

在頂點著色器 3 \_ 0 中，允許四個層級的呼叫嵌套。

只允許轉送的呼叫。 這表示，在頂點著色器中，標籤的位置應該在呼叫指令參考之後。

如果在 [迴圈](loop---vs.md)內部叫用呼叫指令 .。。[endloop](endloop---vs.md) 區塊，可在副程式內部存取 [迴圈計數器 Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) 的值。

如果副程式參考 [迴圈計數器](dx9-graphics-reference-asm-vs-registers-loop-counter.md) 暫存器 (aL) 位於副程式之外，則每個對此副程式的呼叫實例都應該以 [迴圈](loop---vs.md)括住 .。。[endloop](endloop---vs.md) 組塊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
