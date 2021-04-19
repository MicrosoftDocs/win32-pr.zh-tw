---
description: 比較兩個數值資料類型實例或物件的兩個實例，以支援 < 的多載，並傳回兩個實例中較小的一個。 引數的資料類型和傳回值相同。
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: 'XMMin template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986564"
---
# <a name="xmmin-template"></a><span data-ttu-id="744b4-104">XMMin 範本</span><span class="sxs-lookup"><span data-stu-id="744b4-104">XMMin template</span></span>

<span data-ttu-id="744b4-105">比較兩個數值資料類型實例或物件的兩個實例，以支援 < 的多載，並傳回兩個實例中較小的一個。</span><span class="sxs-lookup"><span data-stu-id="744b4-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the smaller one of the two instances.</span></span> <span data-ttu-id="744b4-106">引數的資料類型和傳回值相同。</span><span class="sxs-lookup"><span data-stu-id="744b4-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="744b4-107">語法</span><span class="sxs-lookup"><span data-stu-id="744b4-107">Syntax</span></span>

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="744b4-108">參數</span><span class="sxs-lookup"><span data-stu-id="744b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="744b4-109"><span id="a"></span><span id="A"></span>*的*</span><span class="sxs-lookup"><span data-stu-id="744b4-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="744b4-110">\[在中 \] ，指定兩個物件的第一個。</span><span class="sxs-lookup"><span data-stu-id="744b4-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="744b4-111"><span id="b"></span><span id="B"></span>*B*</span><span class="sxs-lookup"><span data-stu-id="744b4-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="744b4-112">\[在中 \] ，指定兩個物件的其中兩個。</span><span class="sxs-lookup"><span data-stu-id="744b4-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="744b4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="744b4-113">Return Value</span></span>

<span data-ttu-id="744b4-114">傳回兩個輸入物件中較小的一個。</span><span class="sxs-lookup"><span data-stu-id="744b4-114">Returns the smaller of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="744b4-115">備註</span><span class="sxs-lookup"><span data-stu-id="744b4-115">Remarks</span></span>

<span data-ttu-id="744b4-116">`XMMin` 是範本，而且在範本具現化時，會指定 T 類型。</span><span class="sxs-lookup"><span data-stu-id="744b4-116">`XMMin` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="744b4-117">`XMMin`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。</span><span class="sxs-lookup"><span data-stu-id="744b4-117">The `XMMin` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="744b4-118">`XMMin` 可在 XNAMath 2.x 中以宏的形式提供。</span><span class="sxs-lookup"><span data-stu-id="744b4-118">`XMMin` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="744b4-119">在理想情況下，請使用 std：： min 而不是 `XMMin` 。</span><span class="sxs-lookup"><span data-stu-id="744b4-119">Ideally use std::min instead of `XMMin`.</span></span> <span data-ttu-id="744b4-120">若要避免與具有 std：： min 的 Windows 標頭髮生衝突，您必須 \# 先定義 NOMINMAX，然後再包含 windows 標頭。</span><span class="sxs-lookup"><span data-stu-id="744b4-120">To avoid conflicts with Windows headers with std::min, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="744b4-121">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="744b4-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="744b4-122">平台需求</span><span class="sxs-lookup"><span data-stu-id="744b4-122">Platform Requirements</span></span>

<span data-ttu-id="744b4-123">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="744b4-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="744b4-124">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="744b4-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="744b4-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="744b4-125">Requirements</span></span>



| <span data-ttu-id="744b4-126">需求</span><span class="sxs-lookup"><span data-stu-id="744b4-126">Requirement</span></span> | <span data-ttu-id="744b4-127">值</span><span class="sxs-lookup"><span data-stu-id="744b4-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="744b4-128">標頭</span><span class="sxs-lookup"><span data-stu-id="744b4-128">Header</span></span><br/> | <dl> <span data-ttu-id="744b4-129"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="744b4-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="744b4-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="744b4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744b4-131">DirectXMath 程式庫範本函數</span><span class="sxs-lookup"><span data-stu-id="744b4-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="744b4-132">**XMMax**</span><span class="sxs-lookup"><span data-stu-id="744b4-132">**XMMax**</span></span>](xmmax-template.md)
</dt> </dl>

 

 




