---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: 代表用來建立運算子、系結資料表、命令記錄器和其他物件的 DirectML 裝置。
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803741"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="57a8c-103">IDMLDevice1 介面 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="57a8c-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="57a8c-104">代表用來建立運算子、系結資料表、命令記錄器和其他物件的 DirectML 裝置。</span><span class="sxs-lookup"><span data-stu-id="57a8c-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="57a8c-105">**IDMLDevice1** 介面繼承自 [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)。</span><span class="sxs-lookup"><span data-stu-id="57a8c-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="57a8c-106">DirectML 裝置一律會與一個基礎 Direct3D 12 裝置相關聯。</span><span class="sxs-lookup"><span data-stu-id="57a8c-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="57a8c-107">DirectML 裝置所建立的所有物件都會維持其父裝置的強式參考。</span><span class="sxs-lookup"><span data-stu-id="57a8c-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="57a8c-108">不同于 Direct3D 12 裝置，DML 裝置不是 singleton。</span><span class="sxs-lookup"><span data-stu-id="57a8c-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="57a8c-109">因此，您可以透過相同的 Direct3D 12 裝置建立多個 DirectML 裝置。</span><span class="sxs-lookup"><span data-stu-id="57a8c-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="57a8c-110">不過，這不是建議的作法，因為 DirectML 裝置沒有可變動的狀態，因此在相同的 Direct3D 12 裝置上建立多個 DML 裝置並沒有什麼好處。</span><span class="sxs-lookup"><span data-stu-id="57a8c-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="57a8c-111">此物件是安全線程。</span><span class="sxs-lookup"><span data-stu-id="57a8c-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57a8c-112">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="57a8c-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="57a8c-113">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="57a8c-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="57a8c-114">可用性</span><span class="sxs-lookup"><span data-stu-id="57a8c-114">Availability</span></span>
<span data-ttu-id="57a8c-115">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="57a8c-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="57a8c-116">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="57a8c-116">Tensor constraints</span></span>
<span data-ttu-id="57a8c-117">**目標平臺**： Windows</span><span class="sxs-lookup"><span data-stu-id="57a8c-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="57a8c-118">繼承</span><span class="sxs-lookup"><span data-stu-id="57a8c-118">Inheritance</span></span>


<span data-ttu-id="57a8c-119">IDMLDevice1 介面繼承自 IDMLDevice 介面。</span><span class="sxs-lookup"><span data-stu-id="57a8c-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="57a8c-120">方法</span><span class="sxs-lookup"><span data-stu-id="57a8c-120">Methods</span></span>

<p><span data-ttu-id="57a8c-121"><b>IDMLDevice1</b>介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="57a8c-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="57a8c-122">方法</span><span class="sxs-lookup"><span data-stu-id="57a8c-122">Method</span></span> | <span data-ttu-id="57a8c-123">描述</span><span class="sxs-lookup"><span data-stu-id="57a8c-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="57a8c-124">IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="57a8c-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="57a8c-125">將 DirectML 運算子的圖形編譯成可分派至 GPU 的物件。</span><span class="sxs-lookup"><span data-stu-id="57a8c-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="57a8c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="57a8c-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="57a8c-127">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="57a8c-127">**Target Platform**</span></span> | <span data-ttu-id="57a8c-128">Windows</span><span class="sxs-lookup"><span data-stu-id="57a8c-128">Windows</span></span> |
| <span data-ttu-id="57a8c-129">**標頭**</span><span class="sxs-lookup"><span data-stu-id="57a8c-129">**Header**</span></span> | <span data-ttu-id="57a8c-130">directml。h</span><span class="sxs-lookup"><span data-stu-id="57a8c-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="57a8c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57a8c-131">See also</span></span>

[<span data-ttu-id="57a8c-132">IDMLDevice 介面</span><span class="sxs-lookup"><span data-stu-id="57a8c-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)