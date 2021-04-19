---
description: 將另一個緩衝區新增至 ID3DXPRTBuffer，並將結果儲存在 ID3DXPRTBuffer 中。
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'ID3DXPRTBuffer：： AddBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989232"
---
# <a name="id3dxprtbufferaddbuffer-method"></a><span data-ttu-id="074ea-103">ID3DXPRTBuffer：： AddBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="074ea-103">ID3DXPRTBuffer::AddBuffer method</span></span>

<span data-ttu-id="074ea-104">將另一個緩衝區新增至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) ，並將結果儲存在 **ID3DXPRTBuffer** 中。</span><span class="sxs-lookup"><span data-stu-id="074ea-104">Adds another buffer to the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and stores the results in **ID3DXPRTBuffer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="074ea-105">語法</span><span class="sxs-lookup"><span data-stu-id="074ea-105">Syntax</span></span>


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="074ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="074ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074ea-107">*pBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="074ea-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="074ea-108">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="074ea-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="074ea-109">緩衝區的指標，其中包含要加入至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區之個別成員的成員。</span><span class="sxs-lookup"><span data-stu-id="074ea-109">Pointer to a buffer that contains members to be added to the respective members of the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074ea-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="074ea-110">Return value</span></span>

<span data-ttu-id="074ea-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="074ea-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="074ea-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="074ea-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="074ea-113">如果方法失敗，則會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="074ea-113">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="074ea-114">備註</span><span class="sxs-lookup"><span data-stu-id="074ea-114">Remarks</span></span>

<span data-ttu-id="074ea-115">pBuffer 和 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 必須有相同數目的樣本、係數和色彩通道;否則，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="074ea-115">pBuffer and [**ID3DXPRTBuffer**](id3dxprtbuffer.md) must have the same number of samples, coefficients, and color channels; the method will fail otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="074ea-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="074ea-116">Requirements</span></span>



| <span data-ttu-id="074ea-117">需求</span><span class="sxs-lookup"><span data-stu-id="074ea-117">Requirement</span></span> | <span data-ttu-id="074ea-118">值</span><span class="sxs-lookup"><span data-stu-id="074ea-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="074ea-119">標頭</span><span class="sxs-lookup"><span data-stu-id="074ea-119">Header</span></span><br/>  | <dl> <span data-ttu-id="074ea-120"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="074ea-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="074ea-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="074ea-121">Library</span></span><br/> | <dl> <span data-ttu-id="074ea-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="074ea-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="074ea-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="074ea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074ea-124">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="074ea-124">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




