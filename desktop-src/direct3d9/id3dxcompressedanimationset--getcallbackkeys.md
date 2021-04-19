---
description: 使用主要畫面格動畫所用的回呼金鑰資料來填滿陣列。
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'ID3DXCompressedAnimationSet：： GetCallbackKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe56a3dbdd7d019deb5d7111fa592470bffd244d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998366"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="ab8c0-103">ID3DXCompressedAnimationSet：： GetCallbackKeys 方法</span><span class="sxs-lookup"><span data-stu-id="ab8c0-103">ID3DXCompressedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="ab8c0-104">使用主要畫面格動畫所用的回呼金鑰資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="ab8c0-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab8c0-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab8c0-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="ab8c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab8c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab8c0-107">*pCallbackKeys* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab8c0-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab8c0-108">類型： **[ **LPD3DXKEY \_ 回呼**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="ab8c0-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="ab8c0-109">方法用來填滿回呼資料的 [**D3DXKEY \_ 回呼**](d3dxkey-callback.md) 結構之使用者配置陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="ab8c0-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab8c0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab8c0-110">Return value</span></span>

<span data-ttu-id="ab8c0-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab8c0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab8c0-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ab8c0-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ab8c0-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="ab8c0-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab8c0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab8c0-114">Requirements</span></span>



| <span data-ttu-id="ab8c0-115">需求</span><span class="sxs-lookup"><span data-stu-id="ab8c0-115">Requirement</span></span> | <span data-ttu-id="ab8c0-116">值</span><span class="sxs-lookup"><span data-stu-id="ab8c0-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab8c0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ab8c0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ab8c0-118"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab8c0-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ab8c0-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="ab8c0-119">Library</span></span><br/> | <dl> <span data-ttu-id="ab8c0-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab8c0-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab8c0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab8c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab8c0-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="ab8c0-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> <dt>

[<span data-ttu-id="ab8c0-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="ab8c0-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




