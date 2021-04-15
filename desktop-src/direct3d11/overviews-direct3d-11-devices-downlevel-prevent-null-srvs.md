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
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a><span data-ttu-id="e3eec-103">防止不必要的 Null 圖元著色器 SRVs</span><span class="sxs-lookup"><span data-stu-id="e3eec-103">Preventing Unwanted NULL Pixel Shader SRVs</span></span>

<span data-ttu-id="e3eec-104">在 Direct3D 9 圖形硬體上執行的 Direct3D 11 應用程式可能會不慎導致驅動程式收到 **Null** 著色器資源檢視 (SRVs) ，即使應用程式將非 **Null** SRVs 系結至圖元著色器階段。</span><span class="sxs-lookup"><span data-stu-id="e3eec-104">Direct3D 11 applications that run on Direct3D 9 graphics hardware could inadvertently cause the driver to receive **NULL** shader-resource views (SRVs) even when the applications bind non-**NULL** SRVs to the pixel shader stage.</span></span> <span data-ttu-id="e3eec-105">只有當應用程式在應用程式執行時終結 SRVs 時，才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e3eec-105">This situation can occur only if the applications destroy SRVs while they execute.</span></span> <span data-ttu-id="e3eec-106">本主題討論如何解決接收 **null** 著色器資源檢視 (SRVs) 的驅動程式，即使非 **Null** SRVs 系結至圖元著色器階段也是如此。</span><span class="sxs-lookup"><span data-stu-id="e3eec-106">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span>

<span data-ttu-id="e3eec-107">為了防止驅動程式接收不必要的 **Null** SRVs，應用程式必須在每次呼叫 [**>id3d11devicecoNtext：:P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)之前，呼叫 [**>id3d11devicecoNtext：:P Ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources)來取消設定所有 SRVs。</span><span class="sxs-lookup"><span data-stu-id="e3eec-107">To prevent the driver from receiving unwanted **NULL** SRVs, the applications must call [**ID3D11DeviceContext::PSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) to unset all SRVs before each call to [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span></span> <span data-ttu-id="e3eec-108">但是，如果應用程式在程式碼執行結束之前沒有終結 SRVs，就不需要取消設定 SRVs。</span><span class="sxs-lookup"><span data-stu-id="e3eec-108">However, if the applications do not destroy SRVs until the end of their code execution, they do not need to unset the SRVs.</span></span>

<span data-ttu-id="e3eec-109">[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。</span><span class="sxs-lookup"><span data-stu-id="e3eec-109">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3eec-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3eec-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3eec-111">舊版硬體上的 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e3eec-111">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




