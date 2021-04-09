---
description: DirectXMath 程式庫提供許多結構和定義型別來封裝資料，以支援容易使用、優化和可攜性。
ms.assetid: 4b9ffc17-3917-551c-7cb5-19de505dfd21
title: DirectXMath 程式庫類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ac888e451fe1e1ba5cfc66184bf2eb7b6feffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848474"
---
# <a name="directxmath-library-types"></a><span data-ttu-id="c703c-103">DirectXMath 程式庫類型</span><span class="sxs-lookup"><span data-stu-id="c703c-103">DirectXMath Library types</span></span>

<span data-ttu-id="c703c-104">DirectXMath 程式庫提供許多結構和定義型別來封裝資料，以支援容易使用、優化和可攜性。</span><span class="sxs-lookup"><span data-stu-id="c703c-104">The DirectXMath Library provides a number of structures and defined types to encapsulate data to support ease of use, optimization, and portability.</span></span>

<span data-ttu-id="c703c-105">下列清單包含目前 DirectXMath 程式庫的一部分結構，並可透過 DirectXMath. h 標頭取得。</span><span class="sxs-lookup"><span data-stu-id="c703c-105">The list below includes structures currently part of the DirectXMath Library, and available through the DirectXMath.h header.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c703c-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="c703c-106">In this section</span></span>



| <span data-ttu-id="c703c-107">主題</span><span class="sxs-lookup"><span data-stu-id="c703c-107">Topic</span></span>                                                             | <span data-ttu-id="c703c-108">描述</span><span class="sxs-lookup"><span data-stu-id="c703c-108">Description</span></span>                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c703c-109">**半資料類型**</span><span class="sxs-lookup"><span data-stu-id="c703c-109">**HALF Data Type**</span></span>](half-data-type.md)<br/>               | <span data-ttu-id="c703c-110">以16位浮點數組成的 **uint16 \_ t** 的別名，其中包含正負號位、5位偏誤的指數和10位尾數。</span><span class="sxs-lookup"><span data-stu-id="c703c-110">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span><br/>                         |
| [<span data-ttu-id="c703c-111">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="c703c-111">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)<br/>       | <span data-ttu-id="c703c-112">用來代表 4 32 位浮點數或整陣列件向量的可移植型別，每個都能以最佳方式對齊，並對應至硬體向量暫存器。</span><span class="sxs-lookup"><span data-stu-id="c703c-112">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span><br/>       |
| [<span data-ttu-id="c703c-113">**XMVECTORF32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="c703c-113">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)<br/> | <span data-ttu-id="c703c-114">不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將浮點值載入至 [**XMVECTOR**](xmvector-data-type.md) 類型的實例。</span><span class="sxs-lookup"><span data-stu-id="c703c-114">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/> |
| [<span data-ttu-id="c703c-115">**XMVECTORI32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="c703c-115">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)<br/> | <span data-ttu-id="c703c-116">不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法將整數值載入至 [**XMVECTOR**](xmvector-data-type.md) 類型的實例。</span><span class="sxs-lookup"><span data-stu-id="c703c-116">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/>        |
| [<span data-ttu-id="c703c-117">**XMVECTORU32 資料類型**</span><span class="sxs-lookup"><span data-stu-id="c703c-117">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)<br/> | <span data-ttu-id="c703c-118">不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將 uint32 \_ t 值載入至 XMVECTOR 類型的實例。</span><span class="sxs-lookup"><span data-stu-id="c703c-118">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of XMVECTOR type.</span></span><br/>                                    |
| [<span data-ttu-id="c703c-119">**XMVECTORU8 資料類型**</span><span class="sxs-lookup"><span data-stu-id="c703c-119">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)<br/>   | <span data-ttu-id="c703c-120">不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將 uint8 \_ t 值載入 XMVECTOR 類型的實例。</span><span class="sxs-lookup"><span data-stu-id="c703c-120">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of XMVECTOR type.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="c703c-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="c703c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c703c-122">DirectXMath 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="c703c-122">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)
</dt> </dl>

 

 




