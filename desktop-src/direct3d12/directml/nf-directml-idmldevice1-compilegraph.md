---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: 將 DirectML 運算子的圖形編譯成可分派至 GPU 的物件。
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417044"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="da4f7-103">IDMLDevice1：： CompileGraph 方法 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="da4f7-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="da4f7-104">將 DirectML 運算子的圖形編譯成可分派至 GPU 的物件。</span><span class="sxs-lookup"><span data-stu-id="da4f7-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="da4f7-105">已編譯的運算子代表適合在 GPU 上執行之運算子的有效率、內建形式。</span><span class="sxs-lookup"><span data-stu-id="da4f7-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="da4f7-106">已編譯的運算子會保存狀態 (例如著色器和其他物件) 執行所需。</span><span class="sxs-lookup"><span data-stu-id="da4f7-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="da4f7-107">由於編譯的運算子會執行 [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) 介面，因此您可以視需要從 GPU 記憶體中收回一個。</span><span class="sxs-lookup"><span data-stu-id="da4f7-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="da4f7-108">如需詳細資訊，請參閱 [IDMLDevice1：：收回](/windows/win32/api/directml/nf-directml-idmldevice-evict) 和 [IDMLDevice1：： MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) 。</span><span class="sxs-lookup"><span data-stu-id="da4f7-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="da4f7-109">在這個方法傳回之後，編譯的運算子不會使用或參考圖形描述內提供的 [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) 物件。</span><span class="sxs-lookup"><span data-stu-id="da4f7-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da4f7-110">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="da4f7-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="da4f7-111">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="da4f7-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da4f7-112">語法</span><span class="sxs-lookup"><span data-stu-id="da4f7-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="da4f7-113">參數</span><span class="sxs-lookup"><span data-stu-id="da4f7-113">Parameters</span></span>

`desc`

<span data-ttu-id="da4f7-114">類型： **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="da4f7-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="da4f7-115">要編譯之圖形的描述。</span><span class="sxs-lookup"><span data-stu-id="da4f7-115">A description of the graph to compile.</span></span> <span data-ttu-id="da4f7-116">請參閱 [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)。</span><span class="sxs-lookup"><span data-stu-id="da4f7-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="da4f7-117">類型： [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="da4f7-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="da4f7-118">用來控制此運算子執行的任何旗標。</span><span class="sxs-lookup"><span data-stu-id="da4f7-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="da4f7-119">類型： <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="da4f7-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="da4f7-120">全域唯一識別碼的參考， (您想要在 <i>ppv</i>中傳回之介面的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="da4f7-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="da4f7-121">這應該是 [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)的 GUID。</span><span class="sxs-lookup"><span data-stu-id="da4f7-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="da4f7-122">類型： <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="da4f7-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="da4f7-123">記憶體區塊的指標，該區塊會接收已編譯之運算子的指標。</span><span class="sxs-lookup"><span data-stu-id="da4f7-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="da4f7-124">這是 [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)指標的位址，表示已建立的已編譯運算子。</span><span class="sxs-lookup"><span data-stu-id="da4f7-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="da4f7-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="da4f7-125">Return value</span></span>

<span data-ttu-id="da4f7-126">類型： [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="da4f7-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="da4f7-127">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="da4f7-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="da4f7-128">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da4f7-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da4f7-129">備註</span><span class="sxs-lookup"><span data-stu-id="da4f7-129">Remarks</span></span>

<span data-ttu-id="da4f7-130">DirectML 運算子圖形 API 提供了一種可在不同硬體上有效率地使用 DirectML 的抽象方法。</span><span class="sxs-lookup"><span data-stu-id="da4f7-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="da4f7-131">DirectML 會套用 tensor 層級的優化，例如根據所使用的介面卡，選擇最有效率的 tensor 版面配置。</span><span class="sxs-lookup"><span data-stu-id="da4f7-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="da4f7-132">它也會套用優化，例如移除聯結或分割運算子。</span><span class="sxs-lookup"><span data-stu-id="da4f7-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="da4f7-133">建議您在建立 DirectML 圖形之前套用高階優化。</span><span class="sxs-lookup"><span data-stu-id="da4f7-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="da4f7-134">例如，使用 BatchNorm、常數折迭和常見的子運算式刪除來融合加積運算子。</span><span class="sxs-lookup"><span data-stu-id="da4f7-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="da4f7-135">DirectML 圖優化器內的優化目的在於補充這類裝置獨立的優化，通常是由機器學習架構進行一般處理。</span><span class="sxs-lookup"><span data-stu-id="da4f7-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4f7-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="da4f7-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="da4f7-137">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="da4f7-137">**Target Platform**</span></span> | <span data-ttu-id="da4f7-138">Windows</span><span class="sxs-lookup"><span data-stu-id="da4f7-138">Windows</span></span> |
| <span data-ttu-id="da4f7-139">**標頭**</span><span class="sxs-lookup"><span data-stu-id="da4f7-139">**Header**</span></span> | <span data-ttu-id="da4f7-140">directml。h</span><span class="sxs-lookup"><span data-stu-id="da4f7-140">directml.h</span></span> |
| <span data-ttu-id="da4f7-141">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="da4f7-141">**Library**</span></span> | <span data-ttu-id="da4f7-142">DirectML .lib</span><span class="sxs-lookup"><span data-stu-id="da4f7-142">DirectML.lib</span></span> |
| <span data-ttu-id="da4f7-143">**DLL**</span><span class="sxs-lookup"><span data-stu-id="da4f7-143">**DLL**</span></span> | <span data-ttu-id="da4f7-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="da4f7-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="da4f7-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da4f7-145">See also</span></span>

[<span data-ttu-id="da4f7-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="da4f7-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)