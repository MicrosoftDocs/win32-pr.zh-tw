---
description: 以 \_ 16 位浮點數組成的 uint16 t 的別名，其中包含正負號位、5位偏誤的指數和10位尾數。
ms.assetid: E84E0EBA-5C34-41AA-84DB-7A65EBDCAD15
title: '半資料類型 (DirectXPackedVector .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651b84675be68bd433fdeaaae588cb01dc745ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978410"
---
# <a name="half-data-type"></a><span data-ttu-id="65fd3-103">半資料類型</span><span class="sxs-lookup"><span data-stu-id="65fd3-103">HALF Data Type</span></span>

<span data-ttu-id="65fd3-104">以16位浮點數組成的 **uint16 \_ t** 的別名，其中包含正負號位、5位偏誤的指數和10位尾數。</span><span class="sxs-lookup"><span data-stu-id="65fd3-104">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span>


```C++
typedef uint16_t HALF;
```



## <a name="remarks"></a><span data-ttu-id="65fd3-105">備註</span><span class="sxs-lookup"><span data-stu-id="65fd3-105">Remarks</span></span>

<span data-ttu-id="65fd3-106">半資料類型相當於 IEEE 754 binary16 格式。</span><span class="sxs-lookup"><span data-stu-id="65fd3-106">The HALF data type is equivalent to the IEEE 754 binary16 format.</span></span>

<span data-ttu-id="65fd3-107">半 \_ 分鐘 = 6.10352 e-5f</span><span class="sxs-lookup"><span data-stu-id="65fd3-107">HALF\_MIN = 6.10352e-5f</span></span>

<span data-ttu-id="65fd3-108">半 \_ MAX = 65504 f。</span><span class="sxs-lookup"><span data-stu-id="65fd3-108">HALF\_MAX = 65504.f</span></span>

<span data-ttu-id="65fd3-109">如需一半資料類型的詳細資訊，請參閱 [半精確度浮點數格式](https://en.wikipedia.org/wiki/Half_precision_floating-point_format)。</span><span class="sxs-lookup"><span data-stu-id="65fd3-109">For more info about the HALF data type, see [Half-precision floating-point format](https://en.wikipedia.org/wiki/Half_precision_floating-point_format).</span></span>

<span data-ttu-id="65fd3-110">**命名空間**：使用 DirectX：:P ackedvector</span><span class="sxs-lookup"><span data-stu-id="65fd3-110">**Namespace**: Use DirectX::PackedVector</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="65fd3-111">平台需求</span><span class="sxs-lookup"><span data-stu-id="65fd3-111">Platform Requirements</span></span>

<span data-ttu-id="65fd3-112">Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="65fd3-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="65fd3-113">Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。</span><span class="sxs-lookup"><span data-stu-id="65fd3-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="65fd3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="65fd3-114">Requirements</span></span>



| <span data-ttu-id="65fd3-115">需求</span><span class="sxs-lookup"><span data-stu-id="65fd3-115">Requirement</span></span> | <span data-ttu-id="65fd3-116">值</span><span class="sxs-lookup"><span data-stu-id="65fd3-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65fd3-117">標頭</span><span class="sxs-lookup"><span data-stu-id="65fd3-117">Header</span></span><br/> | <dl> <span data-ttu-id="65fd3-118"><dt>DirectXPackedVector。h</dt></span><span class="sxs-lookup"><span data-stu-id="65fd3-118"><dt>DirectXPackedVector.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65fd3-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65fd3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65fd3-120">DirectXMath 程式庫類型</span><span class="sxs-lookup"><span data-stu-id="65fd3-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> </dl>

 

 




