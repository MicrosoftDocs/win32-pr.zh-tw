---
description: 將緩衝區中的每個值乘以常數值。
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'ID3DXPRTBuffer：： ScaleBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992136"
---
# <a name="id3dxprtbufferscalebuffer-method"></a><span data-ttu-id="49591-103">ID3DXPRTBuffer：： ScaleBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="49591-103">ID3DXPRTBuffer::ScaleBuffer method</span></span>

<span data-ttu-id="49591-104">將緩衝區中的每個值乘以常數值。</span><span class="sxs-lookup"><span data-stu-id="49591-104">Multiplies every value in the buffer by a constant value.</span></span>

## <a name="syntax"></a><span data-ttu-id="49591-105">語法</span><span class="sxs-lookup"><span data-stu-id="49591-105">Syntax</span></span>


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="49591-106">參數</span><span class="sxs-lookup"><span data-stu-id="49591-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49591-107">*調整規模* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49591-107">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49591-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49591-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49591-109">用來調整緩衝區的常數值。</span><span class="sxs-lookup"><span data-stu-id="49591-109">Constant value used to scale the buffer.</span></span> <span data-ttu-id="49591-110">緩衝區中的每個值都是由這個值的乘積和原始的緩衝區值所取代。</span><span class="sxs-lookup"><span data-stu-id="49591-110">Every value in the buffer is replaced by the product of this value and the original buffer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49591-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="49591-111">Return value</span></span>

<span data-ttu-id="49591-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49591-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49591-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="49591-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="49591-114">如果方法失敗，則會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="49591-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="49591-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="49591-115">Requirements</span></span>



| <span data-ttu-id="49591-116">需求</span><span class="sxs-lookup"><span data-stu-id="49591-116">Requirement</span></span> | <span data-ttu-id="49591-117">值</span><span class="sxs-lookup"><span data-stu-id="49591-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49591-118">標頭</span><span class="sxs-lookup"><span data-stu-id="49591-118">Header</span></span><br/>  | <dl> <span data-ttu-id="49591-119"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="49591-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="49591-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="49591-120">Library</span></span><br/> | <dl> <span data-ttu-id="49591-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="49591-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49591-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49591-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49591-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="49591-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
