---
description: 複製面板資訊物件。
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'ID3DXSkinInfo：： Clone 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196227"
---
# <a name="id3dxskininfoclone-method"></a><span data-ttu-id="08d66-103">ID3DXSkinInfo：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="08d66-103">ID3DXSkinInfo::Clone method</span></span>

<span data-ttu-id="08d66-104">複製面板資訊物件。</span><span class="sxs-lookup"><span data-stu-id="08d66-104">Clones a skin info object.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d66-105">語法</span><span class="sxs-lookup"><span data-stu-id="08d66-105">Syntax</span></span>


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="08d66-106">參數</span><span class="sxs-lookup"><span data-stu-id="08d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d66-107">*ppSkinInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="08d66-107">*ppSkinInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08d66-108">類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="08d66-108">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="08d66-109">[**ID3DXSkinInfo**](id3dxskininfo.md)物件之指標的位址，如果方法成功，則會包含複製的物件。</span><span class="sxs-lookup"><span data-stu-id="08d66-109">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) object, which will contain the cloned object if the method is successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d66-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="08d66-110">Return value</span></span>

<span data-ttu-id="08d66-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08d66-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08d66-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="08d66-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="08d66-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="08d66-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d66-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="08d66-114">Requirements</span></span>



| <span data-ttu-id="08d66-115">需求</span><span class="sxs-lookup"><span data-stu-id="08d66-115">Requirement</span></span> | <span data-ttu-id="08d66-116">值</span><span class="sxs-lookup"><span data-stu-id="08d66-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08d66-117">標頭</span><span class="sxs-lookup"><span data-stu-id="08d66-117">Header</span></span><br/>  | <dl> <span data-ttu-id="08d66-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="08d66-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="08d66-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="08d66-119">Library</span></span><br/> | <dl> <span data-ttu-id="08d66-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="08d66-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="08d66-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08d66-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d66-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="08d66-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 




