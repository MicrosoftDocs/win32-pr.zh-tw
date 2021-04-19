---
description: 變更緩衝區中包含的樣本數目。
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: 'ID3DXPRTBuffer：： Resize 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c54044ffc9e166131faa16c9b438b497c658ef25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989207"
---
# <a name="id3dxprtbufferresize-method"></a><span data-ttu-id="0eccc-103">ID3DXPRTBuffer：： Resize 方法</span><span class="sxs-lookup"><span data-stu-id="0eccc-103">ID3DXPRTBuffer::Resize method</span></span>

<span data-ttu-id="0eccc-104">變更緩衝區中包含的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="0eccc-104">Changes the number of samples contained in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eccc-105">語法</span><span class="sxs-lookup"><span data-stu-id="0eccc-105">Syntax</span></span>


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a><span data-ttu-id="0eccc-106">參數</span><span class="sxs-lookup"><span data-stu-id="0eccc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eccc-107">*NewSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0eccc-107">*NewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eccc-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0eccc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0eccc-109">要包含在緩衝區中的樣本數。</span><span class="sxs-lookup"><span data-stu-id="0eccc-109">Number of samples to be contained in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eccc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0eccc-110">Return value</span></span>

<span data-ttu-id="0eccc-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0eccc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0eccc-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0eccc-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0eccc-113">如果方法失敗，則會傳回下列值： E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="0eccc-113">If the method fails, the following value will be returned, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eccc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0eccc-114">Requirements</span></span>



| <span data-ttu-id="0eccc-115">需求</span><span class="sxs-lookup"><span data-stu-id="0eccc-115">Requirement</span></span> | <span data-ttu-id="0eccc-116">值</span><span class="sxs-lookup"><span data-stu-id="0eccc-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0eccc-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0eccc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0eccc-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="0eccc-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0eccc-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0eccc-119">Library</span></span><br/> | <dl> <span data-ttu-id="0eccc-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0eccc-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0eccc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0eccc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eccc-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="0eccc-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
