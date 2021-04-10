---
title: 互通性
description: 描述 Direct2D 如何與其他系統交互操作。
ms.assetid: 538e0ff7-50a8-40e2-ab34-d3eb6b7d0c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 872a090980618548fd73e43c6f82644962b8bd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092813"
---
# <a name="interoperability"></a><span data-ttu-id="2ca44-103">互通性</span><span class="sxs-lookup"><span data-stu-id="2ca44-103">Interoperability</span></span>

<span data-ttu-id="2ca44-104">本節中的主題描述 Direct2D 如何與其他系統（例如 GDI、Direct3D 和 WIC）交互操作。</span><span class="sxs-lookup"><span data-stu-id="2ca44-104">The topics in this section describe how Direct2D interoperates with other systems, such as GDI, Direct3D, and WIC.</span></span>

> [!Note]  
> <span data-ttu-id="2ca44-105">從 Windows 8 開始，Direct2D 會提供 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 介面，以提供簡單的交互操作方式。</span><span class="sxs-lookup"><span data-stu-id="2ca44-105">Starting with Windows 8, Direct2D provides the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface which provides a simple way to interoperate.</span></span> <span data-ttu-id="2ca44-106">如需詳細資訊，請參閱「 [裝置」和「裝置](devices-and-device-contexts.md) 內容」主題。</span><span class="sxs-lookup"><span data-stu-id="2ca44-106">See the [Devices and Device Contexts](devices-and-device-contexts.md) topic for more info.</span></span>

 



| <span data-ttu-id="2ca44-107">主題</span><span class="sxs-lookup"><span data-stu-id="2ca44-107">Topic</span></span>                                                                                                           | <span data-ttu-id="2ca44-108">描述</span><span class="sxs-lookup"><span data-stu-id="2ca44-108">Description</span></span>                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ca44-109">互通性概觀</span><span class="sxs-lookup"><span data-stu-id="2ca44-109">Interoperability Overview</span></span>](interoperability-overview.md)<br/>                                           | <span data-ttu-id="2ca44-110">摘要說明您可以搭配 Direct2D 使用的各種技術。</span><span class="sxs-lookup"><span data-stu-id="2ca44-110">Summarizes the different technologies you can use with Direct2D.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="2ca44-111">Direct2D 和 GDI 互通性總覽</span><span class="sxs-lookup"><span data-stu-id="2ca44-111">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)<br/>           | <span data-ttu-id="2ca44-112">說明如何搭配使用 Direct2D 和 GDI。</span><span class="sxs-lookup"><span data-stu-id="2ca44-112">Describes how to use Direct2D and GDI together.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="2ca44-113">比較 Direct2D 和 GDI 硬體加速</span><span class="sxs-lookup"><span data-stu-id="2ca44-113">Comparing Direct2D and GDI Hardware Acceleration</span></span>](comparing-direct2d-and-gdi.md)<br/>                   | <span data-ttu-id="2ca44-114">[Direct2D](./direct2d-portal.md) 和 [GDI](/windows/desktop/gdi/windows-gdi) 都是立即模式2d 轉譯 api，兩者都提供某種程度的硬體加速。</span><span class="sxs-lookup"><span data-stu-id="2ca44-114">[Direct2D](./direct2d-portal.md) and [GDI](/windows/desktop/gdi/windows-gdi) are both immediate mode 2D rendering APIs and both offer some degree of hardware acceleration.</span></span> <span data-ttu-id="2ca44-115">本主題探討 Direct2D 與 GDI 之間的差異，包括過去和目前這兩個 Api 的硬體加速功能差異。</span><span class="sxs-lookup"><span data-stu-id="2ca44-115">This topic explores the differences between Direct2D and GDI, including past and present differences in the hardware acceleration features of both APIs.</span></span><br/> |
| [<span data-ttu-id="2ca44-116">Direct2D 和 Direct3D 互通性概觀</span><span class="sxs-lookup"><span data-stu-id="2ca44-116">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)<br/> | <span data-ttu-id="2ca44-117">說明如何搭配使用 Direct2D 和 Direct3D 10。</span><span class="sxs-lookup"><span data-stu-id="2ca44-117">Describes how to use Direct2D and Direct3D 10 together.</span></span><br/>                                                                                                                                                                                                                                                                     |



 

 

