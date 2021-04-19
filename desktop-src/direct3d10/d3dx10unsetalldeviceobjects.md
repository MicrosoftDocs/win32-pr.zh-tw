---
description: 將所有資源的指標設為 Null，以移除裝置中的所有資源。 這應該會在應用程式關閉時呼叫。 這有助於確保當某個資源釋出所有資源時，都不會將這些資源系結至裝置。
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: 'D3DX10UnsetAllDeviceObjects 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976488"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a><span data-ttu-id="074e3-105">D3DX10UnsetAllDeviceObjects 函式</span><span class="sxs-lookup"><span data-stu-id="074e3-105">D3DX10UnsetAllDeviceObjects function</span></span>

<span data-ttu-id="074e3-106">將所有資源的指標設為 **Null**，以移除裝置中的所有資源。</span><span class="sxs-lookup"><span data-stu-id="074e3-106">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="074e3-107">這應該會在應用程式關閉時呼叫。</span><span class="sxs-lookup"><span data-stu-id="074e3-107">This should be called during shutdown of your application.</span></span> <span data-ttu-id="074e3-108">這有助於確保當某個資源釋出所有資源時，都不會將這些資源系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="074e3-108">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="074e3-109">語法</span><span class="sxs-lookup"><span data-stu-id="074e3-109">Syntax</span></span>


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="074e3-110">參數</span><span class="sxs-lookup"><span data-stu-id="074e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074e3-111">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="074e3-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="074e3-112">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="074e3-112">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="074e3-113">裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="074e3-113">Pointer to the device.</span></span> <span data-ttu-id="074e3-114">請參閱 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)。</span><span class="sxs-lookup"><span data-stu-id="074e3-114">See [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074e3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="074e3-115">Return value</span></span>

<span data-ttu-id="074e3-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="074e3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="074e3-117">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="074e3-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="074e3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="074e3-118">Requirements</span></span>



| <span data-ttu-id="074e3-119">需求</span><span class="sxs-lookup"><span data-stu-id="074e3-119">Requirement</span></span> | <span data-ttu-id="074e3-120">值</span><span class="sxs-lookup"><span data-stu-id="074e3-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="074e3-121">標頭</span><span class="sxs-lookup"><span data-stu-id="074e3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="074e3-122"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="074e3-122"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="074e3-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="074e3-123">Library</span></span><br/> | <dl> <span data-ttu-id="074e3-124"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="074e3-124"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="074e3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="074e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074e3-126">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="074e3-126">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




