---
title: 磚的資源不支援樣板格式
description: 磚的資源不支援包含樣板的格式。
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020727"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a>磚的資源不支援樣板格式

磚的資源不支援包含樣板的格式。

包含樣板的格式包括 DXGI \_ 格式 \_ D24 \_ UNORM \_ S8 \_ UINT (以及 R24G8 系列中的相關格式、) 系列中的相關格式、 \_ \_ D32 \_ 浮點數 \_ S8X24 FLOAT R32G8X24 \_ UINT (以及系列) 中的相關格式。

某些實作將深度和樣板儲存在不同的配置中，其他則將它們儲存在一起。 兩個配置的磚管理會有不同，而且單一 API 無法抽象或合理化差異。 我們建議未來硬體支援獨立深度和樣板表面，每個獨立並排顯示。 32位深度會有128x128 圖格，而8位樣板會有256x256 磚。 因此，應用程式需要接受深度與樣板之間的動態磚形狀不對齊。 但在不同的轉譯目標表面格式，已經有相同的問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源跨進程和裝置共用](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




