---
title: 'ID3DX11ThreadPump WaitForAllItems 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 等候執行緒抽取中的所有工作專案完成。
ms.assetid: 6dfdaee8-e563-4c37-a2c1-4b115e29c434
keywords:
- WaitForAllItems 方法 Direct3D 11
- WaitForAllItems 方法 Direct3D 11，ID3DX11ThreadPump 介面
- ID3DX11ThreadPump 介面 Direct3D 11，WaitForAllItems 方法
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.WaitForAllItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40abbab67d6743be2190d5e81c733f63b52b32f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992230"
---
# <a name="id3dx11threadpumpwaitforallitems-method"></a><span data-ttu-id="807cf-107">ID3DX11ThreadPump：： WaitForAllItems 方法</span><span class="sxs-lookup"><span data-stu-id="807cf-107">ID3DX11ThreadPump::WaitForAllItems method</span></span>

> [!Note]  
> <span data-ttu-id="807cf-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="807cf-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="807cf-109">等候執行緒抽取中的所有工作專案完成。</span><span class="sxs-lookup"><span data-stu-id="807cf-109">Waits for all work items in the thread pump to finish.</span></span>

## <a name="syntax"></a><span data-ttu-id="807cf-110">語法</span><span class="sxs-lookup"><span data-stu-id="807cf-110">Syntax</span></span>


```C++
HRESULT WaitForAllItems();
```



## <a name="parameters"></a><span data-ttu-id="807cf-111">參數</span><span class="sxs-lookup"><span data-stu-id="807cf-111">Parameters</span></span>

<span data-ttu-id="807cf-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="807cf-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="807cf-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="807cf-113">Return value</span></span>

<span data-ttu-id="807cf-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="807cf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="807cf-115">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="807cf-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="807cf-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="807cf-116">Requirements</span></span>



| <span data-ttu-id="807cf-117">需求</span><span class="sxs-lookup"><span data-stu-id="807cf-117">Requirement</span></span> | <span data-ttu-id="807cf-118">值</span><span class="sxs-lookup"><span data-stu-id="807cf-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="807cf-119">標頭</span><span class="sxs-lookup"><span data-stu-id="807cf-119">Header</span></span><br/>  | <dl> <span data-ttu-id="807cf-120"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="807cf-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="807cf-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="807cf-121">Library</span></span><br/> | <dl> <span data-ttu-id="807cf-122"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="807cf-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="807cf-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="807cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="807cf-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="807cf-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="807cf-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="807cf-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





