---
description: 取得儲存已壓縮之主要畫面格動畫資料的資料緩衝區。
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'ID3DXCompressedAnimationSet：： GetCompressedData 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7907daf5db2d03afca310a630f6aeb2dc16c4f22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981835"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a><span data-ttu-id="367bc-103">ID3DXCompressedAnimationSet：： GetCompressedData 方法</span><span class="sxs-lookup"><span data-stu-id="367bc-103">ID3DXCompressedAnimationSet::GetCompressedData method</span></span>

<span data-ttu-id="367bc-104">取得儲存已壓縮之主要畫面格動畫資料的資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="367bc-104">Gets the data buffer that stores compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="367bc-105">語法</span><span class="sxs-lookup"><span data-stu-id="367bc-105">Syntax</span></span>


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="367bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="367bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="367bc-107">*ppCompressedData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="367bc-107">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="367bc-108">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="367bc-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="367bc-109">[**ID3DXBuffer**](id3dxbuffer.md)資料緩衝區指標的位址，該緩衝區會接收壓縮的主要畫面格動畫資料。</span><span class="sxs-lookup"><span data-stu-id="367bc-109">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) data buffer that receives compressed key frame animation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="367bc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="367bc-110">Return value</span></span>

<span data-ttu-id="367bc-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="367bc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="367bc-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="367bc-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="367bc-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="367bc-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="367bc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="367bc-114">Requirements</span></span>



| <span data-ttu-id="367bc-115">需求</span><span class="sxs-lookup"><span data-stu-id="367bc-115">Requirement</span></span> | <span data-ttu-id="367bc-116">值</span><span class="sxs-lookup"><span data-stu-id="367bc-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="367bc-117">標頭</span><span class="sxs-lookup"><span data-stu-id="367bc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="367bc-118"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="367bc-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="367bc-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="367bc-119">Library</span></span><br/> | <dl> <span data-ttu-id="367bc-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="367bc-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="367bc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="367bc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="367bc-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="367bc-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




