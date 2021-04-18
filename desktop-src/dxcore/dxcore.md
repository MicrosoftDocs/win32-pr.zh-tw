---
title: DXCore
description: DXCore 是適用于 DirectX 裝置的介面卡列舉 API。
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: 80e93ac7440629a809cb01b4d1d4fa2e73b7ee91
ms.sourcegitcommit: aa021b23d7e8bba2e1df9de93a1c315a17681810
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/10/2020
ms.locfileid: "106966071"
---
# <a name="dxcore"></a><span data-ttu-id="8e2b9-103">DXCore</span><span class="sxs-lookup"><span data-stu-id="8e2b9-103">DXCore</span></span>

<span data-ttu-id="8e2b9-104">DXCore 是圖形和計算裝置的介面卡列舉 API，因此其某些設備會與 [DXGI](../direct3ddxgi/dx-graphics-dxgi.md)的部分重迭。</span><span class="sxs-lookup"><span data-stu-id="8e2b9-104">DXCore is an adapter enumeration API for graphics and compute devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span> <span data-ttu-id="8e2b9-105">DXCore 是由 Direct3D 12 使用。</span><span class="sxs-lookup"><span data-stu-id="8e2b9-105">DXCore is used by Direct3D 12.</span></span>

<span data-ttu-id="8e2b9-106">此檔集包含使用 DXCore 進行程式設計的相關資訊，以及 DXCore 參考。</span><span class="sxs-lookup"><span data-stu-id="8e2b9-106">This documentation set contains information about programming with DXCore, as well as the DXCore reference.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e2b9-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e2b9-107">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8e2b9-108">**支援的執行時間環境**</span><span class="sxs-lookup"><span data-stu-id="8e2b9-108">**Supported runtime environments**</span></span> | <span data-ttu-id="8e2b9-109">Windows/c + +</span><span class="sxs-lookup"><span data-stu-id="8e2b9-109">Windows/C++</span></span> |
| <span data-ttu-id="8e2b9-110">**建議的程式設計語言**</span><span class="sxs-lookup"><span data-stu-id="8e2b9-110">**Recommended programming languages**</span></span> | <span data-ttu-id="8e2b9-111">C++</span><span class="sxs-lookup"><span data-stu-id="8e2b9-111">C++</span></span> |
| <span data-ttu-id="8e2b9-112">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="8e2b9-112">**Minimum supported client**</span></span> | <span data-ttu-id="8e2b9-113">Windows 10，版本 2004 (10.0;組建 19041) </span><span class="sxs-lookup"><span data-stu-id="8e2b9-113">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="8e2b9-114">**標頭**</span><span class="sxs-lookup"><span data-stu-id="8e2b9-114">**Header**</span></span> | <span data-ttu-id="8e2b9-115">dxcore .h 和 dxcore_interface。h</span><span class="sxs-lookup"><span data-stu-id="8e2b9-115">dxcore.h and dxcore_interface.h</span></span> |
| <span data-ttu-id="8e2b9-116">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="8e2b9-116">**Library**</span></span> | <span data-ttu-id="8e2b9-117">dxcore .lib</span><span class="sxs-lookup"><span data-stu-id="8e2b9-117">dxcore.lib</span></span> |
| <span data-ttu-id="8e2b9-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="8e2b9-118">**DLL**</span></span> | <span data-ttu-id="8e2b9-119">dxcore.dll</span><span class="sxs-lookup"><span data-stu-id="8e2b9-119">dxcore.dll</span></span> |

## <a name="in-this-section"></a><span data-ttu-id="8e2b9-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="8e2b9-120">In this section</span></span>

| <span data-ttu-id="8e2b9-121">主題</span><span class="sxs-lookup"><span data-stu-id="8e2b9-121">Topic</span></span> | <span data-ttu-id="8e2b9-122">描述</span><span class="sxs-lookup"><span data-stu-id="8e2b9-122">Description</span></span> |
|-|-|
| [<span data-ttu-id="8e2b9-123">DXCore 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="8e2b9-123">DXCore programming guide</span></span>](dxcore-programming-guide.md) | <span data-ttu-id="8e2b9-124">使用 DXCore 進行程式設計的指引。</span><span class="sxs-lookup"><span data-stu-id="8e2b9-124">Guidance for programming with DXCore.</span></span> |
| [<span data-ttu-id="8e2b9-125">DXCore 參考</span><span class="sxs-lookup"><span data-stu-id="8e2b9-125">DXCore reference</span></span>](dxcore-reference.md) | <span data-ttu-id="8e2b9-126">本節涵蓋在 DXCore 中宣告的 DXCore Api，以及 dxcore_interface .h。</span><span class="sxs-lookup"><span data-stu-id="8e2b9-126">This section covers DXCore APIs declared in dxcore.h and dxcore_interface.h.</span></span> |
