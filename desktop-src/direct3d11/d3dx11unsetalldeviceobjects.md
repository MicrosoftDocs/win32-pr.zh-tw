---
title: 'D3DX11UnsetAllDeviceObjects 函式 (D3DX11core) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 >id3d11devicecoNtext ClearState 方法。
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- D3DX11UnsetAllDeviceObjects 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323112"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a><span data-ttu-id="da0c2-105">D3DX11UnsetAllDeviceObjects 函式</span><span class="sxs-lookup"><span data-stu-id="da0c2-105">D3DX11UnsetAllDeviceObjects function</span></span>

> [!Note]  
> <span data-ttu-id="da0c2-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="da0c2-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="da0c2-107">我們建議您使用 [**>id3d11devicecoNtext：： ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) 方法，而不是使用此函數。</span><span class="sxs-lookup"><span data-stu-id="da0c2-107">Instead of using this function, we recommend that you use the [**ID3D11DeviceContext::ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) method.</span></span>

 

<span data-ttu-id="da0c2-108">將所有資源的指標設為 **Null**，以移除裝置中的所有資源。</span><span class="sxs-lookup"><span data-stu-id="da0c2-108">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="da0c2-109">這應該會在應用程式關閉時呼叫。</span><span class="sxs-lookup"><span data-stu-id="da0c2-109">This should be called during shutdown of your application.</span></span> <span data-ttu-id="da0c2-110">這有助於確保當某個資源釋出所有資源時，都不會將這些資源系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="da0c2-110">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0c2-111">語法</span><span class="sxs-lookup"><span data-stu-id="da0c2-111">Syntax</span></span>


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="da0c2-112">參數</span><span class="sxs-lookup"><span data-stu-id="da0c2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da0c2-113">*pCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da0c2-113">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0c2-114">類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="da0c2-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="da0c2-115">[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="da0c2-115">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da0c2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="da0c2-116">Return value</span></span>

<span data-ttu-id="da0c2-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da0c2-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da0c2-118">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="da0c2-118">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da0c2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="da0c2-119">Requirements</span></span>



| <span data-ttu-id="da0c2-120">需求</span><span class="sxs-lookup"><span data-stu-id="da0c2-120">Requirement</span></span> | <span data-ttu-id="da0c2-121">值</span><span class="sxs-lookup"><span data-stu-id="da0c2-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da0c2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="da0c2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="da0c2-123"><dt>D3DX11core。h</dt></span><span class="sxs-lookup"><span data-stu-id="da0c2-123"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="da0c2-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="da0c2-124">Library</span></span><br/> | <dl> <span data-ttu-id="da0c2-125"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da0c2-125"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da0c2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da0c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0c2-127">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="da0c2-127">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





