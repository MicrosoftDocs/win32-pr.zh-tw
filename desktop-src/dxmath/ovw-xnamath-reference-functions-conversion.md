---
description: 列出 DirectXMath 所提供的轉換函數。
ms.assetid: 6a0a8422-991d-00aa-0fd7-b41387adc72e
title: DirectXMath 程式庫轉換函式
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d182089d766043d47459e859503e48c0c59c2407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993028"
---
# <a name="directxmath-library-conversion-functions"></a><span data-ttu-id="00714-103">DirectXMath 程式庫轉換函式</span><span class="sxs-lookup"><span data-stu-id="00714-103">DirectXMath Library conversion functions</span></span>

<span data-ttu-id="00714-104">列出 DirectXMath 所提供的轉換函數。</span><span class="sxs-lookup"><span data-stu-id="00714-104">Lists the conversion functions provided by DirectXMath.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="00714-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="00714-105">In this section</span></span>



| <span data-ttu-id="00714-106">主題</span><span class="sxs-lookup"><span data-stu-id="00714-106">Topic</span></span>                                                                       | <span data-ttu-id="00714-107">描述</span><span class="sxs-lookup"><span data-stu-id="00714-107">Description</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00714-108">**XMConvertFloatToHalf**</span><span class="sxs-lookup"><span data-stu-id="00714-108">**XMConvertFloatToHalf**</span></span>](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalf)<br/>             | <span data-ttu-id="00714-109">將單精確度浮點數轉換為半精確度浮點值。</span><span class="sxs-lookup"><span data-stu-id="00714-109">Converts a single-precision floating-point value to a half-precision floating-point value.</span></span><br/>                                                                |
| [<span data-ttu-id="00714-110">**XMConvertFloatToHalfStream**</span><span class="sxs-lookup"><span data-stu-id="00714-110">**XMConvertFloatToHalfStream**</span></span>](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalfstream)<br/> | <span data-ttu-id="00714-111">將單精確度浮點數的資料流程轉換成半精確度浮點值的資料流程。</span><span class="sxs-lookup"><span data-stu-id="00714-111">Converts a stream of single-precision floating-point values to a stream of half-precision floating-point values.</span></span><br/>                                          |
| [<span data-ttu-id="00714-112">**XMConvertHalfToFloat**</span><span class="sxs-lookup"><span data-stu-id="00714-112">**XMConvertHalfToFloat**</span></span>](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconverthalftofloat)<br/>             | <span data-ttu-id="00714-113">將半精確度浮點數轉換成單精確度浮點值。</span><span class="sxs-lookup"><span data-stu-id="00714-113">Converts a half-precision floating-point value to a single-precision floating-point value.</span></span><br/>                                                                |
| [<span data-ttu-id="00714-114">**XMConvertHalfToFloatStream**</span><span class="sxs-lookup"><span data-stu-id="00714-114">**XMConvertHalfToFloatStream**</span></span>](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconverthalftofloatstream)<br/> | <span data-ttu-id="00714-115">將半精確度浮點數的資料流程轉換成單精確度浮點值的資料流程。</span><span class="sxs-lookup"><span data-stu-id="00714-115">Converts a stream of half-precision floating-point values to a stream of single-precision floating-point values.</span></span><br/>                                          |
| [<span data-ttu-id="00714-116">**XMConvertToDegrees**</span><span class="sxs-lookup"><span data-stu-id="00714-116">**XMConvertToDegrees**</span></span>](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttodegrees)<br/>                 | <span data-ttu-id="00714-117">將以弧度為單位的角度，轉換成以度數測量的角度。</span><span class="sxs-lookup"><span data-stu-id="00714-117">Converts an angle measured in radians into one measured in degrees.</span></span><br/>                                                                                       |
| [<span data-ttu-id="00714-118">**XMConvertToRadians**</span><span class="sxs-lookup"><span data-stu-id="00714-118">**XMConvertToRadians**</span></span>](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttoradians)<br/>                 | <span data-ttu-id="00714-119">將以度為單位的角度，轉換成以弧度為單位的角度。</span><span class="sxs-lookup"><span data-stu-id="00714-119">Converts an angle measured in degrees into one measured in radians.</span></span><br/>                                                                                       |
| [<span data-ttu-id="00714-120">**XMConvertVectorFloatToInt**</span><span class="sxs-lookup"><span data-stu-id="00714-120">**XMConvertVectorFloatToInt**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmconvertvectorfloattoint)<br/>   | <span data-ttu-id="00714-121">將具有 **float** 元件的 [**XMVECTOR**](xmvector-data-type.md)轉換成具有 **int32 \_ t** 元件的 **XMVECTOR** ，並套用統一偏差。</span><span class="sxs-lookup"><span data-stu-id="00714-121">Converts an [**XMVECTOR**](xmvector-data-type.md) with **float** components to an **XMVECTOR** with **int32\_t** components and applies a uniform bias.</span></span><br/>  |
| [<span data-ttu-id="00714-122">**XMConvertVectorFloatToUInt**</span><span class="sxs-lookup"><span data-stu-id="00714-122">**XMConvertVectorFloatToUInt**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmconvertvectorfloattouint)<br/> | <span data-ttu-id="00714-123">將具有 **float** 元件的 [**XMVECTOR**](xmvector-data-type.md)轉換成具有 **uint32 \_ t** 元件的 **XMVECTOR** ，並套用統一偏差。</span><span class="sxs-lookup"><span data-stu-id="00714-123">Converts an [**XMVECTOR**](xmvector-data-type.md) with **float** components to an **XMVECTOR** with **uint32\_t** components and applies a uniform bias.</span></span><br/> |
| [<span data-ttu-id="00714-124">**XMConvertVectorIntToFloat**</span><span class="sxs-lookup"><span data-stu-id="00714-124">**XMConvertVectorIntToFloat**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmconvertvectorinttofloat)<br/>   | <span data-ttu-id="00714-125">將具有 **int32 \_ t** 元件的 [**XMVECTOR**](xmvector-data-type.md)轉換成具有 **float** 元件的 **XMVECTOR** ，並套用統一偏差。</span><span class="sxs-lookup"><span data-stu-id="00714-125">Converts an [**XMVECTOR**](xmvector-data-type.md) with **int32\_t** components to an **XMVECTOR** with **float** components and applies a uniform bias.</span></span><br/>  |
| [<span data-ttu-id="00714-126">**XMConvertVectorUIntToFloat**</span><span class="sxs-lookup"><span data-stu-id="00714-126">**XMConvertVectorUIntToFloat**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmconvertvectoruinttofloat)<br/> | <span data-ttu-id="00714-127">將具有 **uint32 \_ t** 元件的 [**XMVECTOR**](xmvector-data-type.md)轉換為具有 **float** 元件的 **XMVECTOR** ，並套用統一偏差。</span><span class="sxs-lookup"><span data-stu-id="00714-127">Converts an [**XMVECTOR**](xmvector-data-type.md) with **uint32\_t** components to an **XMVECTOR** with **float** components and applies a uniform bias.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="00714-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="00714-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00714-129">DirectXMath 程式庫函式</span><span class="sxs-lookup"><span data-stu-id="00714-129">DirectXMath Library Functions</span></span>](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
