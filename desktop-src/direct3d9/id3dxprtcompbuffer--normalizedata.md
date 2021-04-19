---
description: 將所有主體元件分析正規化 (PCA) 權數，使其介於-1 到1之間。 基礎向量會經過修改，以反映此正規化。
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'ID3DXPRTCompBuffer：： NormalizeData 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982232"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a><span data-ttu-id="6128a-104">ID3DXPRTCompBuffer：： NormalizeData 方法</span><span class="sxs-lookup"><span data-stu-id="6128a-104">ID3DXPRTCompBuffer::NormalizeData method</span></span>

<span data-ttu-id="6128a-105">將所有主體元件分析正規化 (PCA) 權數，使其介於-1 到1之間。</span><span class="sxs-lookup"><span data-stu-id="6128a-105">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="6128a-106">基礎向量會經過修改，以反映此正規化。</span><span class="sxs-lookup"><span data-stu-id="6128a-106">Basis vectors are modified to reflect this normalization.</span></span>

## <a name="syntax"></a><span data-ttu-id="6128a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6128a-107">Syntax</span></span>


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a><span data-ttu-id="6128a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6128a-108">Parameters</span></span>

<span data-ttu-id="6128a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6128a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6128a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6128a-110">Return value</span></span>

<span data-ttu-id="6128a-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6128a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6128a-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6128a-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6128a-113">如果方法失敗，則會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="6128a-113">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="6128a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6128a-114">Requirements</span></span>



| <span data-ttu-id="6128a-115">需求</span><span class="sxs-lookup"><span data-stu-id="6128a-115">Requirement</span></span> | <span data-ttu-id="6128a-116">值</span><span class="sxs-lookup"><span data-stu-id="6128a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6128a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6128a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6128a-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6128a-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6128a-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="6128a-119">Library</span></span><br/> | <dl> <span data-ttu-id="6128a-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6128a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6128a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6128a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6128a-122">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="6128a-122">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




