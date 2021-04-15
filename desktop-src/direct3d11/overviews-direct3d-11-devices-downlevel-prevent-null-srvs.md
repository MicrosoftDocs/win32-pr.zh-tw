---
title: 防止不必要的 Null 圖元著色器 SRVs
description: 本主題討論如何解決接收 Null 著色器資源檢視 (SRVs) 的驅動程式，即使非 Null SRVs 系結至圖元著色器階段也是如此。
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bacacf7704cffe12df44b9b0be667632307adb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990655"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a>防止不必要的 Null 圖元著色器 SRVs

在 Direct3D 9 圖形硬體上執行的 Direct3D 11 應用程式可能會不慎導致驅動程式收到 **Null** 著色器資源檢視 (SRVs) ，即使應用程式將非 **Null** SRVs 系結至圖元著色器階段。 只有當應用程式在應用程式執行時終結 SRVs 時，才會發生這種情況。 本主題討論如何解決接收 **null** 著色器資源檢視 (SRVs) 的驅動程式，即使非 **Null** SRVs 系結至圖元著色器階段也是如此。

為了防止驅動程式接收不必要的 **Null** SRVs，應用程式必須在每次呼叫 [**>id3d11devicecoNtext：:P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)之前，呼叫 [**>id3d11devicecoNtext：:P Ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources)來取消設定所有 SRVs。 但是，如果應用程式在程式碼執行結束之前沒有終結 SRVs，就不需要取消設定 SRVs。

[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[舊版硬體上的 Direct3D 11](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




