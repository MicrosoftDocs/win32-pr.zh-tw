---
title: D3DPERF_QueryRepeatFrame 函式
description: 判斷效能分析工具是否要求將目前的框架重新提交給 Direct3D 以進行效能分析。 PIX 目前不支援此函式。
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "103681503"
---
# <a name="d3dperf_queryrepeatframe-function"></a><span data-ttu-id="4615c-104">D3DPERF_QueryRepeatFrame 函式</span><span class="sxs-lookup"><span data-stu-id="4615c-104">D3DPERF_QueryRepeatFrame function</span></span>

<span data-ttu-id="4615c-105">判斷效能分析工具是否要求將目前的框架重新提交給 Direct3D 以進行效能分析。</span><span class="sxs-lookup"><span data-stu-id="4615c-105">Determine whether a performance profiler is requesting that the current frame be resubmitted to Direct3D for performance analysis.</span></span> <span data-ttu-id="4615c-106">PIX 目前不支援此函式。</span><span class="sxs-lookup"><span data-stu-id="4615c-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="4615c-107">語法</span><span class="sxs-lookup"><span data-stu-id="4615c-107">Syntax</span></span>

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a><span data-ttu-id="4615c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4615c-108">Return value</span></span>

<span data-ttu-id="4615c-109">如果傳回值為 TRUE，則呼叫端應該重複相同的呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="4615c-109">If the return value is TRUE, the caller should repeat the same sequence of calls.</span></span> <span data-ttu-id="4615c-110">如果為 FALSE，則呼叫端應該繼續。</span><span class="sxs-lookup"><span data-stu-id="4615c-110">If FALSE, the caller should continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="4615c-111">備註</span><span class="sxs-lookup"><span data-stu-id="4615c-111">Remarks</span></span>

<span data-ttu-id="4615c-112">函式應該在 IDirect3DDevice9 之後立即呼叫：會呼叫 **:P** 重新傳送。</span><span class="sxs-lookup"><span data-stu-id="4615c-112">The function should be called immediately after **IDirect3DDevice9::Present** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="4615c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4615c-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4615c-114">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="4615c-114">**Target Platform**</span></span> | <span data-ttu-id="4615c-115">Windows</span><span class="sxs-lookup"><span data-stu-id="4615c-115">Windows</span></span> |
| <span data-ttu-id="4615c-116">**標頭**</span><span class="sxs-lookup"><span data-stu-id="4615c-116">**Header**</span></span> | <span data-ttu-id="4615c-117">d3d9。h</span><span class="sxs-lookup"><span data-stu-id="4615c-117">d3d9.h</span></span> |
| <span data-ttu-id="4615c-118">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="4615c-118">**Library**</span></span> | <span data-ttu-id="4615c-119">d3d9 .lib</span><span class="sxs-lookup"><span data-stu-id="4615c-119">d3d9.lib</span></span> |
| <span data-ttu-id="4615c-120">**DLL**</span><span class="sxs-lookup"><span data-stu-id="4615c-120">**DLL**</span></span> | <span data-ttu-id="4615c-121">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="4615c-121">d3d9.dll</span></span> |