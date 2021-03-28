---
title: 'ID3DX11DataLoader 摧毀方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 在工作專案完成後終結載入器。
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- 終結方法 Direct3D 11
- 終結方法 Direct3D 11，ID3DX11DataLoader 介面
- ID3DX11DataLoader 介面 Direct3D 11，摧毀方法
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c3a1c6511a00d66704c104b3b69150a8509e41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974723"
---
# <a name="id3dx11dataloaderdestroy-method"></a><span data-ttu-id="1d0af-107">ID3DX11DataLoader：:D estroy 方法</span><span class="sxs-lookup"><span data-stu-id="1d0af-107">ID3DX11DataLoader::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="1d0af-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1d0af-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="1d0af-109">在工作專案完成後終結載入器。</span><span class="sxs-lookup"><span data-stu-id="1d0af-109">Destroys the loader after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0af-110">語法</span><span class="sxs-lookup"><span data-stu-id="1d0af-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="1d0af-111">參數</span><span class="sxs-lookup"><span data-stu-id="1d0af-111">Parameters</span></span>

<span data-ttu-id="1d0af-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1d0af-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d0af-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d0af-113">Return value</span></span>

<span data-ttu-id="1d0af-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d0af-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d0af-115">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1d0af-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0af-116">備註</span><span class="sxs-lookup"><span data-stu-id="1d0af-116">Remarks</span></span>

<span data-ttu-id="1d0af-117">[**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="1d0af-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0af-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d0af-118">Requirements</span></span>



| <span data-ttu-id="1d0af-119">需求</span><span class="sxs-lookup"><span data-stu-id="1d0af-119">Requirement</span></span> | <span data-ttu-id="1d0af-120">值</span><span class="sxs-lookup"><span data-stu-id="1d0af-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0af-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1d0af-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1d0af-122"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d0af-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="1d0af-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d0af-123">Library</span></span><br/> | <dl> <span data-ttu-id="1d0af-124"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d0af-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d0af-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d0af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0af-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="1d0af-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="1d0af-127">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="1d0af-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





