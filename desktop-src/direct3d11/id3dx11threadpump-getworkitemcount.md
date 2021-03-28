---
title: 'ID3DX11ThreadPump GetWorkItemCount 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 取得執行緒抽取中的工作專案數。
ms.assetid: 04883b25-64dc-41a3-849f-710a59e9d3da
keywords:
- GetWorkItemCount 方法 Direct3D 11
- GetWorkItemCount 方法 Direct3D 11，ID3DX11ThreadPump 介面
- ID3DX11ThreadPump 介面 Direct3D 11，GetWorkItemCount 方法
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetWorkItemCount
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29668e66dd3d8c6d29cbfc69a4ef12a2fdfd18b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974529"
---
# <a name="id3dx11threadpumpgetworkitemcount-method"></a><span data-ttu-id="1e34c-107">ID3DX11ThreadPump：： GetWorkItemCount 方法</span><span class="sxs-lookup"><span data-stu-id="1e34c-107">ID3DX11ThreadPump::GetWorkItemCount method</span></span>

> [!Note]  
> <span data-ttu-id="1e34c-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1e34c-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="1e34c-109">取得執行緒抽取中的工作專案數。</span><span class="sxs-lookup"><span data-stu-id="1e34c-109">Gets the number of work items in the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e34c-110">語法</span><span class="sxs-lookup"><span data-stu-id="1e34c-110">Syntax</span></span>


```C++
UINT GetWorkItemCount();
```



## <a name="parameters"></a><span data-ttu-id="1e34c-111">參數</span><span class="sxs-lookup"><span data-stu-id="1e34c-111">Parameters</span></span>

<span data-ttu-id="1e34c-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1e34c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e34c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e34c-113">Return value</span></span>

<span data-ttu-id="1e34c-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1e34c-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1e34c-115">線上程抽取中排入佇列的工作專案數。</span><span class="sxs-lookup"><span data-stu-id="1e34c-115">The number of work items queued in the thread pump.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e34c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e34c-116">Requirements</span></span>



| <span data-ttu-id="1e34c-117">需求</span><span class="sxs-lookup"><span data-stu-id="1e34c-117">Requirement</span></span> | <span data-ttu-id="1e34c-118">值</span><span class="sxs-lookup"><span data-stu-id="1e34c-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e34c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="1e34c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1e34c-120"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e34c-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="1e34c-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="1e34c-121">Library</span></span><br/> | <dl> <span data-ttu-id="1e34c-122"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e34c-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e34c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e34c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e34c-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="1e34c-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="1e34c-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="1e34c-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

