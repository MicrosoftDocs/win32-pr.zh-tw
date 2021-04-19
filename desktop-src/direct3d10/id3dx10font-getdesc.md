---
description: 取得目前字型物件的描述。
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'ID3DX10Font：： GetDesc 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974874"
---
# <a name="id3dx10fontgetdesc-method"></a><span data-ttu-id="684bc-103">ID3DX10Font：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="684bc-103">ID3DX10Font::GetDesc method</span></span>

<span data-ttu-id="684bc-104">取得目前字型物件的描述。</span><span class="sxs-lookup"><span data-stu-id="684bc-104">Get a description of the current font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="684bc-105">語法</span><span class="sxs-lookup"><span data-stu-id="684bc-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="684bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="684bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="684bc-107">*pDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="684bc-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="684bc-108">類型： **[ **D3DX10 \_ 字型 \_ DESC**](d3dx10-font-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="684bc-108">Type: **[**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="684bc-109">描述字型物件之 [**D3DX10 \_ 字型 \_ DESC**](d3dx10-font-desc.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="684bc-109">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure that describes the font object.</span></span> <span data-ttu-id="684bc-110">如果已定義 UNICODE，則會傳回 D3DX10FONT DESCW 的指標， \_ 否則會傳回 D3DX10FONT DESCA 的指標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="684bc-110">If UNICODE is defined, a pointer to a D3DX10FONT\_DESCW is returned; otherwise a pointer to a D3DX10FONT\_DESCA is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="684bc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="684bc-111">Return value</span></span>

<span data-ttu-id="684bc-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="684bc-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="684bc-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="684bc-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="684bc-114">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="684bc-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="684bc-115">備註</span><span class="sxs-lookup"><span data-stu-id="684bc-115">Remarks</span></span>

<span data-ttu-id="684bc-116">如果已定義 UNICODE，則這個方法會描述 Unicode 字型物件。</span><span class="sxs-lookup"><span data-stu-id="684bc-116">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="684bc-117">否則會呼叫 GetDescA，它會傳回 D3DX10FONT \_ DESCA 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="684bc-117">Otherwise GetDescA is called, which returns a pointer to the D3DX10FONT\_DESCA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="684bc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="684bc-118">Requirements</span></span>



| <span data-ttu-id="684bc-119">需求</span><span class="sxs-lookup"><span data-stu-id="684bc-119">Requirement</span></span> | <span data-ttu-id="684bc-120">值</span><span class="sxs-lookup"><span data-stu-id="684bc-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="684bc-121">標頭</span><span class="sxs-lookup"><span data-stu-id="684bc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="684bc-122"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="684bc-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="684bc-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="684bc-123">Library</span></span><br/> | <dl> <span data-ttu-id="684bc-124"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="684bc-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="684bc-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="684bc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684bc-126">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="684bc-126">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="684bc-127">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="684bc-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




