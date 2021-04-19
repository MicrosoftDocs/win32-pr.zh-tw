---
description: 取得目前字型物件的描述。 GetDescW 和 GetDescA 與這個方法相同，不同之處在于指標會分別傳回至 D3DXFONT \_ DESCW 或 D3DXFONT \_ DESCA 結構。
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'ID3DXFont：： GetDesc 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976704"
---
# <a name="id3dxfontgetdesc-method"></a><span data-ttu-id="9bf67-104">ID3DXFont：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="9bf67-104">ID3DXFont::GetDesc method</span></span>

<span data-ttu-id="9bf67-105">取得目前字型物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9bf67-105">Gets a description of the current font object.</span></span> <span data-ttu-id="9bf67-106">GetDescW 和 GetDescA 與這個方法相同，不同之處在于指標會分別傳回至 [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) 或 **D3DXFONT \_ DESCA** 結構。</span><span class="sxs-lookup"><span data-stu-id="9bf67-106">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf67-107">語法</span><span class="sxs-lookup"><span data-stu-id="9bf67-107">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="9bf67-108">參數</span><span class="sxs-lookup"><span data-stu-id="9bf67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bf67-109">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9bf67-109">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf67-110">類型： **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="9bf67-110">Type: **[**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="9bf67-111">描述字型物件之 [**D3DXFONT \_ DESC**](d3dxfont-desc.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9bf67-111">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure that describes the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bf67-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9bf67-112">Return value</span></span>

<span data-ttu-id="9bf67-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9bf67-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9bf67-114">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9bf67-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9bf67-115">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="9bf67-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bf67-116">備註</span><span class="sxs-lookup"><span data-stu-id="9bf67-116">Remarks</span></span>

<span data-ttu-id="9bf67-117">如果已定義 UNICODE，則這個方法會描述 Unicode 字型物件。</span><span class="sxs-lookup"><span data-stu-id="9bf67-117">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="9bf67-118">否則會呼叫 GetDescA，它會傳回 [**D3DXFONT \_ DESCA**](d3dxfont-desc.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9bf67-118">Otherwise GetDescA is called, which returns a pointer to the [**D3DXFONT\_DESCA**](d3dxfont-desc.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf67-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bf67-119">Requirements</span></span>



| <span data-ttu-id="9bf67-120">需求</span><span class="sxs-lookup"><span data-stu-id="9bf67-120">Requirement</span></span> | <span data-ttu-id="9bf67-121">值</span><span class="sxs-lookup"><span data-stu-id="9bf67-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf67-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9bf67-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9bf67-123"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="9bf67-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9bf67-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="9bf67-124">Library</span></span><br/> | <dl> <span data-ttu-id="9bf67-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bf67-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9bf67-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bf67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf67-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="9bf67-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




