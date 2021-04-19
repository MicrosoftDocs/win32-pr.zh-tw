---
description: 不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將 uint8 \_ t 值載入 XMVECTOR 類型的實例。
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: 'XMVECTORU8 資料類型 (DirectXMath .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982070"
---
# <a name="xmvectoru8-data-type"></a><span data-ttu-id="0b105-103">XMVECTORU8 資料類型</span><span class="sxs-lookup"><span data-stu-id="0b105-103">XMVECTORU8 Data Type</span></span>

<span data-ttu-id="0b105-104">不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將 uint8 \_ t 值載入 [**XMVECTOR**](xmvector-data-type.md) 類型的實例。</span><span class="sxs-lookup"><span data-stu-id="0b105-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a><span data-ttu-id="0b105-105">備註</span><span class="sxs-lookup"><span data-stu-id="0b105-105">Remarks</span></span>

<span data-ttu-id="0b105-106">如需使用 c + + 進行程式設計時可使用 XMVECTORU8 的其他功能（例如，如函式和運算子）的清單，請參閱 [XMVECTORU8 擴充](ovw-xmvectoru8-extensions.md)功能。</span><span class="sxs-lookup"><span data-stu-id="0b105-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU8 when programming in C++, see [XMVECTORU8 Extensions](ovw-xmvectoru8-extensions.md).</span></span>

<span data-ttu-id="0b105-107">[**XMVECTORF32**](xmvectorf32-data-type.md)、 [**XMVECTORU32**](xmvectoru32-data-type.md)、 [**XMVECTORI32**](xmvectori32-data-type.md)和 **XMVECTORU8** 結構是以機制的形式提供，可從不同的常數資料類型建立 [**XMVECTOR**](xmvector-data-type.md) ， (浮點數、不帶正負號整數、整數和位元組) 使用初始化運算式。</span><span class="sxs-lookup"><span data-stu-id="0b105-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and **XMVECTORU8** structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="0b105-108">這是支援 [**XMVECTOR**](xmvector-data-type.md)的必要動作，因為它本身不支援初始化運算式，因為可攜性和優化原因。</span><span class="sxs-lookup"><span data-stu-id="0b105-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="0b105-109">例如：</span><span class="sxs-lookup"><span data-stu-id="0b105-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

<span data-ttu-id="0b105-110">**命名空間**：使用 DirectX</span><span class="sxs-lookup"><span data-stu-id="0b105-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="0b105-111">平台需求</span><span class="sxs-lookup"><span data-stu-id="0b105-111">Platform Requirements</span></span>

<span data-ttu-id="0b105-112">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="0b105-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="0b105-113">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="0b105-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b105-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b105-114">Requirements</span></span>



| <span data-ttu-id="0b105-115">需求</span><span class="sxs-lookup"><span data-stu-id="0b105-115">Requirement</span></span> | <span data-ttu-id="0b105-116">值</span><span class="sxs-lookup"><span data-stu-id="0b105-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b105-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0b105-117">Header</span></span><br/> | <dl> <span data-ttu-id="0b105-118"><dt>DirectXMath。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b105-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b105-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b105-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b105-120">DirectXMath 程式庫類型</span><span class="sxs-lookup"><span data-stu-id="0b105-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="0b105-121">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="0b105-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="0b105-122">**XMVECTORF32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="0b105-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="0b105-123">**XMVECTORI32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="0b105-123">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="0b105-124">**XMVECTORU32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="0b105-124">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="0b105-125">XMVECTORU8 延伸模組</span><span class="sxs-lookup"><span data-stu-id="0b105-125">XMVECTORU8 Extensions</span></span>](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




