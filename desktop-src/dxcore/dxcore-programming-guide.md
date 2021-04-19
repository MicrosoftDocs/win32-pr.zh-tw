---
title: DXCore 程式設計指南
description: 使用 DXCore 進行程式設計的指引。
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: 475469f027d3db2e4a29673c5a674990192a2fe3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965666"
---
# <a name="dxcore-programming-guide"></a><span data-ttu-id="0ead3-103">DXCore 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="0ead3-103">DXCore programming guide</span></span>

<span data-ttu-id="0ead3-104">DXCore 是適用于 DirectX 裝置的介面卡列舉 API，因此其某些設備會與 [DXGI](../direct3ddxgi/dx-graphics-dxgi.md)的部分重迭。</span><span class="sxs-lookup"><span data-stu-id="0ead3-104">DXCore is an adapter enumeration API for DirectX devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0ead3-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="0ead3-105">In this section</span></span>

| <span data-ttu-id="0ead3-106">主題</span><span class="sxs-lookup"><span data-stu-id="0ead3-106">Topic</span></span> | <span data-ttu-id="0ead3-107">描述</span><span class="sxs-lookup"><span data-stu-id="0ead3-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="0ead3-108">使用 DXCore 來列舉介面卡</span><span class="sxs-lookup"><span data-stu-id="0ead3-108">Using DXCore to enumerate adapters</span></span>](dxcore-enum-adapters.md) | <span data-ttu-id="0ead3-109">查看 DXCore 的主要功能，並提供一些程式碼範例，以及最基本 DXCore 應用程式的完整源代碼清單。</span><span class="sxs-lookup"><span data-stu-id="0ead3-109">A look at the main features of DXCore with some code examples, as well as a full source code listing of a minimal DXCore application.</span></span> |
| [<span data-ttu-id="0ead3-110">最低 DXCore 應用程式</span><span class="sxs-lookup"><span data-stu-id="0ead3-110">Minimal DXCore application</span></span>](dxcore-source-code.md) | <span data-ttu-id="0ead3-111">最基本 DXCore 應用程式的完整原始碼清單。</span><span class="sxs-lookup"><span data-stu-id="0ead3-111">The full source code listing for a minimal DXCore application.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="0ead3-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ead3-112">Related topics</span></span>

* [<span data-ttu-id="0ead3-113">DXCore 參考</span><span class="sxs-lookup"><span data-stu-id="0ead3-113">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="0ead3-114">Direct3D 12 圖形</span><span class="sxs-lookup"><span data-stu-id="0ead3-114">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)