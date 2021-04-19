---
description: 不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將 uint32 \_ t 值載入至 XMVECTOR 類型的實例。
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: 'XMVECTORU32 資料類型 (Directxmath .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977562"
---
# <a name="xmvectoru32-data-type"></a><span data-ttu-id="016e5-103">XMVECTORU32 資料類型</span><span class="sxs-lookup"><span data-stu-id="016e5-103">XMVECTORU32 Data Type</span></span>

<span data-ttu-id="016e5-104">不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將 uint32 \_ t 值載入至 [**XMVECTOR**](xmvector-data-type.md) 類型的實例。</span><span class="sxs-lookup"><span data-stu-id="016e5-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a><span data-ttu-id="016e5-105">備註</span><span class="sxs-lookup"><span data-stu-id="016e5-105">Remarks</span></span>

<span data-ttu-id="016e5-106">如需使用 c + + 進行程式設計時可使用 XMVECTORU32 的其他功能（例如，如函式和運算子）的清單，請參閱 [XMVECTORU32 擴充](ovw-xmvectoru32-extensions.md)功能。</span><span class="sxs-lookup"><span data-stu-id="016e5-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU32 when programming in C++, see [XMVECTORU32 Extensions](ovw-xmvectoru32-extensions.md).</span></span>

<span data-ttu-id="016e5-107">[**XMVECTORF32**](xmvectorf32-data-type.md)、 **XMVECTORU32**、 [**XMVECTORI32**](xmvectori32-data-type.md)和 [**XMVECTORU8**](xmvectoru8-data-type.md)結構是以機制的形式提供，可從不同的常數資料類型建立 [**XMVECTOR**](xmvector-data-type.md) ， (浮點數、不帶正負號整數、整數和位元組) 使用初始化運算式。</span><span class="sxs-lookup"><span data-stu-id="016e5-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="016e5-108">這是支援 [**XMVECTOR**](xmvector-data-type.md)的必要動作，因為它本身不支援初始化運算式，因為可攜性和優化原因。</span><span class="sxs-lookup"><span data-stu-id="016e5-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="016e5-109">例如：</span><span class="sxs-lookup"><span data-stu-id="016e5-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

<span data-ttu-id="016e5-110">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="016e5-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="016e5-111">平台需求</span><span class="sxs-lookup"><span data-stu-id="016e5-111">Platform Requirements</span></span>

<span data-ttu-id="016e5-112">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="016e5-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="016e5-113">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="016e5-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="016e5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="016e5-114">Requirements</span></span>



| <span data-ttu-id="016e5-115">需求</span><span class="sxs-lookup"><span data-stu-id="016e5-115">Requirement</span></span> | <span data-ttu-id="016e5-116">值</span><span class="sxs-lookup"><span data-stu-id="016e5-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="016e5-117">標頭</span><span class="sxs-lookup"><span data-stu-id="016e5-117">Header</span></span><br/> | <dl> <span data-ttu-id="016e5-118"><dt>Directxmath。h</dt></span><span class="sxs-lookup"><span data-stu-id="016e5-118"><dt>Directxmath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="016e5-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="016e5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016e5-120">DirectXMath 程式庫類型</span><span class="sxs-lookup"><span data-stu-id="016e5-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="016e5-121">**XMVECTORI32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="016e5-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="016e5-122">**XMVECTORF32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="016e5-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="016e5-123">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="016e5-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="016e5-124">**XMVECTORU8 資料類型**</span><span class="sxs-lookup"><span data-stu-id="016e5-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="016e5-125">XMVECTORU32 延伸模組</span><span class="sxs-lookup"><span data-stu-id="016e5-125">XMVECTORU32 Extensions</span></span>](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




