---
description: 不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法將整數值載入至 XMVECTOR 類型的實例。
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: 'XMVECTORI32 資料類型 (DirectXMath .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995505"
---
# <a name="xmvectori32-data-type"></a><span data-ttu-id="cca8c-103">XMVECTORI32 資料類型</span><span class="sxs-lookup"><span data-stu-id="cca8c-103">XMVECTORI32 Data Type</span></span>

<span data-ttu-id="cca8c-104">不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法將整數值載入至 [**XMVECTOR**](xmvector-data-type.md) 類型的實例。</span><span class="sxs-lookup"><span data-stu-id="cca8c-104">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a><span data-ttu-id="cca8c-105">備註</span><span class="sxs-lookup"><span data-stu-id="cca8c-105">Remarks</span></span>

<span data-ttu-id="cca8c-106">如需在 c + + 中進行程式設計時可使用的其他功能（例如，如函式和運算子）的清單， `XMVECTORI32` 請參閱 [XMVECTORI32 延伸](ovw-xmvectori32-extensions.md)模組。</span><span class="sxs-lookup"><span data-stu-id="cca8c-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORI32` when programming in C++, see [XMVECTORI32 Extensions](ovw-xmvectori32-extensions.md).</span></span>

<span data-ttu-id="cca8c-107">[**XMVECTORF32**](xmvectorf32-data-type.md)、 [**XMVECTORU32**](xmvectoru32-data-type.md)、 **XMVECTORI32** 和 [**XMVECTORU8**](xmvectoru8-data-type.md)結構是以機制的形式提供，可從不同的常數資料類型建立 [**XMVECTOR**](xmvector-data-type.md) ， (浮點數、不帶正負號整數、整數和位元組) 使用初始化運算式。</span><span class="sxs-lookup"><span data-stu-id="cca8c-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32**, and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="cca8c-108">這是支援 [**XMVECTOR**](xmvector-data-type.md)的必要動作，因為它本身不支援初始化運算式，因為可攜性和優化原因。</span><span class="sxs-lookup"><span data-stu-id="cca8c-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="cca8c-109">例如：</span><span class="sxs-lookup"><span data-stu-id="cca8c-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



<span data-ttu-id="cca8c-110">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="cca8c-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="cca8c-111">平台需求</span><span class="sxs-lookup"><span data-stu-id="cca8c-111">Platform Requirements</span></span>

<span data-ttu-id="cca8c-112">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="cca8c-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="cca8c-113">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="cca8c-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="cca8c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cca8c-114">Requirements</span></span>



| <span data-ttu-id="cca8c-115">需求</span><span class="sxs-lookup"><span data-stu-id="cca8c-115">Requirement</span></span> | <span data-ttu-id="cca8c-116">值</span><span class="sxs-lookup"><span data-stu-id="cca8c-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca8c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="cca8c-117">Header</span></span><br/> | <dl> <span data-ttu-id="cca8c-118"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="cca8c-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca8c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cca8c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca8c-120">DirectXMath 程式庫類型</span><span class="sxs-lookup"><span data-stu-id="cca8c-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="cca8c-121">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="cca8c-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="cca8c-122">**XMVECTORF32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="cca8c-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="cca8c-123">**XMVECTORU32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="cca8c-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="cca8c-124">**XMVECTORU8 資料類型**</span><span class="sxs-lookup"><span data-stu-id="cca8c-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="cca8c-125">**XMVECTORI32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="cca8c-125">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> </dl>

 

 




