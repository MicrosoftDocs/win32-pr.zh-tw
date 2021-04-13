---
description: 捕獲 TEXTMETRIC 結構中所識別的字型特性。 這個方法支援 ANSI 和 Unicode 編譯器設定。
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'ID3DXFont：： GetTextMetrics 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322883"
---
# <a name="id3dxfontgettextmetrics-method"></a><span data-ttu-id="b9e7e-104">ID3DXFont：： GetTextMetrics 方法</span><span class="sxs-lookup"><span data-stu-id="b9e7e-104">ID3DXFont::GetTextMetrics method</span></span>

<span data-ttu-id="b9e7e-105">捕獲 [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) 結構中所識別的字型特性。</span><span class="sxs-lookup"><span data-stu-id="b9e7e-105">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="b9e7e-106">這個方法支援 ANSI 和 Unicode 編譯器設定。</span><span class="sxs-lookup"><span data-stu-id="b9e7e-106">This method supports ANSI and Unicode compiler settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e7e-107">語法</span><span class="sxs-lookup"><span data-stu-id="b9e7e-107">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="b9e7e-108">參數</span><span class="sxs-lookup"><span data-stu-id="b9e7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e7e-109">*pTextMetrics* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b9e7e-109">*pTextMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e7e-110">類型： **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span><span class="sxs-lookup"><span data-stu-id="b9e7e-110">Type: **[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span></span>

<span data-ttu-id="b9e7e-111">[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)結構的指標，其中包含字型屬性。</span><span class="sxs-lookup"><span data-stu-id="b9e7e-111">Pointer to a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure, which contains font properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e7e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9e7e-112">Return value</span></span>

<span data-ttu-id="b9e7e-113">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9e7e-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9e7e-114">如果函式成功則為非零，否則為 0。</span><span class="sxs-lookup"><span data-stu-id="b9e7e-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e7e-115">備註</span><span class="sxs-lookup"><span data-stu-id="b9e7e-115">Remarks</span></span>

<span data-ttu-id="b9e7e-116">編譯器設定也會決定結構類型。</span><span class="sxs-lookup"><span data-stu-id="b9e7e-116">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="b9e7e-117">如果已定義 Unicode，函數會傳回 TEXTMETRICW 結構。</span><span class="sxs-lookup"><span data-stu-id="b9e7e-117">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="b9e7e-118">否則，函式呼叫會傳回 TEXTMETRICA 結構。</span><span class="sxs-lookup"><span data-stu-id="b9e7e-118">Otherwise, the function call returns a TEXTMETRICA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e7e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9e7e-119">Requirements</span></span>



| <span data-ttu-id="b9e7e-120">需求</span><span class="sxs-lookup"><span data-stu-id="b9e7e-120">Requirement</span></span> | <span data-ttu-id="b9e7e-121">值</span><span class="sxs-lookup"><span data-stu-id="b9e7e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e7e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b9e7e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b9e7e-123"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e7e-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b9e7e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9e7e-124">Library</span></span><br/> | <dl> <span data-ttu-id="b9e7e-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9e7e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9e7e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9e7e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e7e-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="b9e7e-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
