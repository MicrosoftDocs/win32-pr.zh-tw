---
description: 將儲存的材質裝訂邊資料套用至 ID3DXPRTBuffer 材質緩衝區。
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'ID3DXPRTBuffer：： EvalGH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982244"
---
# <a name="id3dxprtbufferevalgh-method"></a><span data-ttu-id="152b8-103">ID3DXPRTBuffer：： EvalGH 方法</span><span class="sxs-lookup"><span data-stu-id="152b8-103">ID3DXPRTBuffer::EvalGH method</span></span>

<span data-ttu-id="152b8-104">將儲存的材質裝訂邊資料套用至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="152b8-104">Applies stored texture gutter data to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="152b8-105">語法</span><span class="sxs-lookup"><span data-stu-id="152b8-105">Syntax</span></span>


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a><span data-ttu-id="152b8-106">參數</span><span class="sxs-lookup"><span data-stu-id="152b8-106">Parameters</span></span>

<span data-ttu-id="152b8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="152b8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="152b8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="152b8-108">Return value</span></span>

<span data-ttu-id="152b8-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="152b8-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="152b8-110">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="152b8-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="152b8-111">如果方法失敗，則會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="152b8-111">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="152b8-112">備註</span><span class="sxs-lookup"><span data-stu-id="152b8-112">Remarks</span></span>

<span data-ttu-id="152b8-113">這個方法會對 [**ID3DXTextureGutterHelper：： ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) 進行內部呼叫，以抓取並套用材質裝訂邊資料。</span><span class="sxs-lookup"><span data-stu-id="152b8-113">This method makes an internal call to [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) to retrieve and apply texture gutter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="152b8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="152b8-114">Requirements</span></span>



| <span data-ttu-id="152b8-115">需求</span><span class="sxs-lookup"><span data-stu-id="152b8-115">Requirement</span></span> | <span data-ttu-id="152b8-116">值</span><span class="sxs-lookup"><span data-stu-id="152b8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="152b8-117">標頭</span><span class="sxs-lookup"><span data-stu-id="152b8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="152b8-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="152b8-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="152b8-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="152b8-119">Library</span></span><br/> | <dl> <span data-ttu-id="152b8-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="152b8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="152b8-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="152b8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152b8-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="152b8-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




