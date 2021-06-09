---
description: 本主題說明 DirectXMath 程式庫的內部設計。
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: 程式庫內部
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7c1843a83a81e7acac241c66dd18ff26217569
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827232"
---
# <a name="library-internals"></a><span data-ttu-id="4871b-103">程式庫內部</span><span class="sxs-lookup"><span data-stu-id="4871b-103">Library Internals</span></span>

<span data-ttu-id="4871b-104">本主題說明 DirectXMath 程式庫的內部設計。</span><span class="sxs-lookup"><span data-stu-id="4871b-104">This topic describes the internal design of the DirectXMath library.</span></span>

-   [<span data-ttu-id="4871b-105">呼叫慣例</span><span class="sxs-lookup"><span data-stu-id="4871b-105">Calling Conventions</span></span>](#calling-conventions)
-   [<span data-ttu-id="4871b-106">圖形程式庫類型等價</span><span class="sxs-lookup"><span data-stu-id="4871b-106">Graphics Library Type Equivalence</span></span>](#graphics-library-type-equivalence)
-   [<span data-ttu-id="4871b-107">DirectXMath 程式庫中的全域常數</span><span class="sxs-lookup"><span data-stu-id="4871b-107">Global Constants in the DirectXMath Library</span></span>](#global-constants-in-the-directxmath-library)
-   [<span data-ttu-id="4871b-108">Windows SSE 與 SSE2</span><span class="sxs-lookup"><span data-stu-id="4871b-108">Windows SSE versus SSE2</span></span>](#windows-sse-versus-sse2)
-   [<span data-ttu-id="4871b-109">常式變數</span><span class="sxs-lookup"><span data-stu-id="4871b-109">Routine Variants</span></span>](#routine-variants)
-   [<span data-ttu-id="4871b-110">平臺不一致</span><span class="sxs-lookup"><span data-stu-id="4871b-110">Platform Inconsistencies</span></span>](#platform-inconsistencies)
-   [<span data-ttu-id="4871b-111">平臺特定的擴充功能</span><span class="sxs-lookup"><span data-stu-id="4871b-111">Platform-specific Extensions</span></span>](#platform-specific-extensions)
-   [<span data-ttu-id="4871b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="4871b-112">Related topics</span></span>](#related-topics)

## <a name="calling-conventions"></a><span data-ttu-id="4871b-113">呼叫慣例</span><span class="sxs-lookup"><span data-stu-id="4871b-113">Calling Conventions</span></span>

<span data-ttu-id="4871b-114">若要增強可攜性並將資料版面配置優化，您必須針對 DirectXMath 程式庫所支援的每個平臺使用適當的呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="4871b-114">To enhance portability and optimize data layout, you need to use the appropriate calling conventions for each platform supported by the DirectXMath Library.</span></span> <span data-ttu-id="4871b-115">具體而言，當您傳遞 [**XMVECTOR**](xmvector-data-type.md) 物件做為參數（定義為在16位元組界限上對齊）時，會有不同的呼叫需求集合，視目標平臺而定：</span><span class="sxs-lookup"><span data-stu-id="4871b-115">Specifically, when you pass [**XMVECTOR**](xmvector-data-type.md) objects as parameters, which are defined as aligned on a 16-byte boundary, there are different sets of calling requirements, depending on the target platform:</span></span>

<span data-ttu-id="4871b-116">**適用于32位 Windows**</span><span class="sxs-lookup"><span data-stu-id="4871b-116">**For 32-bit Windows**</span></span>

<span data-ttu-id="4871b-117">針對32位的 Windows，有兩個呼叫慣例可用來有效率地傳遞 [ \_ \_ m128](/cpp/cpp/m128)值， (可在該平臺) 上執行 [**XMVECTOR**](xmvector-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="4871b-117">For 32-bit Windows, there are two calling conventions available for efficient passing of [\_\_m128](/cpp/cpp/m128) values (which implements [**XMVECTOR**](xmvector-data-type.md) on that platform).</span></span> <span data-ttu-id="4871b-118">標準是 [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall)，它可以傳遞前三個 [ \_ \_ m128](/cpp/cpp/m128)值 (**XMVECTOR** 實例，) 為 *SSE/SSE2* 登錄中函式的引數。</span><span class="sxs-lookup"><span data-stu-id="4871b-118">The standard is [\_\_fastcall](https://docs.microsoft.com/cpp/cpp/fastcall), which can pass the first three [\_\_m128](/cpp/cpp/m128) values (**XMVECTOR** instances) as arguments to a function in a *SSE/SSE2* register.</span></span> <span data-ttu-id="4871b-119">[ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall)會透過堆疊傳遞其餘的引數。</span><span class="sxs-lookup"><span data-stu-id="4871b-119">[\_\_fastcall](https://docs.microsoft.com/cpp/cpp/fastcall) passes remaining arguments via the stack.</span></span>

<span data-ttu-id="4871b-120">較新的 Microsoft Visual Studio 編譯器支援新的呼叫慣例 \_ \_ vectorcall，最多可傳遞六個 [ \_ \_ m128](/cpp/cpp/m128)值 ([**XMVECTOR**](xmvector-data-type.md)實例) 為 *SSE/SSE2* 暫存器中函式的引數。</span><span class="sxs-lookup"><span data-stu-id="4871b-120">Newer Microsoft Visual Studio compilers support a new calling convention, \_\_vectorcall, which can pass up to six [\_\_m128](/cpp/cpp/m128) values ([**XMVECTOR**](xmvector-data-type.md) instances) as arguments to a function in a *SSE/SSE2* register.</span></span> <span data-ttu-id="4871b-121">如果有足夠的空間，也可以透過 *SSE/SSE2* 暫存器，傳遞異類向量匯總 (也稱為 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) 。</span><span class="sxs-lookup"><span data-stu-id="4871b-121">It can also pass heterogeneous vector aggregates (also known as [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) via *SSE/SSE2* registers if there is sufficient room.</span></span>

<span data-ttu-id="4871b-122">**適用于 Windows 的64位版本**</span><span class="sxs-lookup"><span data-stu-id="4871b-122">**For 64-bit editions of Windows**</span></span>

<span data-ttu-id="4871b-123">針對64位的 Windows，有兩個呼叫慣例可用來有效率地傳遞[ \_ \_ m128](/cpp/cpp/m128)值。</span><span class="sxs-lookup"><span data-stu-id="4871b-123">For 64-bit Windows, there are two calling conventions available for efficient passing of [\_\_m128](/cpp/cpp/m128) values.</span></span> <span data-ttu-id="4871b-124">標準是[ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall)，它會傳遞堆疊上的所有[ \_ \_ m128](/cpp/cpp/m128)值。</span><span class="sxs-lookup"><span data-stu-id="4871b-124">The standard is [\_\_fastcall](https://docs.microsoft.com/cpp/cpp/fastcall), which passes all [\_\_m128](/cpp/cpp/m128) values on the stack.</span></span>

<span data-ttu-id="4871b-125">較新的 Visual Studio 編譯器支援 \_ \_ vectorcall 呼叫慣例，其最多可傳遞六個 [ \_ \_ m128](/cpp/cpp/m128)值 ([**XMVECTOR**](xmvector-data-type.md)實例) 為 *SSE/SSE2* 登錄中函式的引數。</span><span class="sxs-lookup"><span data-stu-id="4871b-125">Newer Visual Studio compilers support the \_\_vectorcall calling convention, which can pass up to six [\_\_m128](/cpp/cpp/m128) values ([**XMVECTOR**](xmvector-data-type.md) instances) as arguments to a function in a *SSE/SSE2* register.</span></span> <span data-ttu-id="4871b-126">如果有足夠的空間，也可以透過 *SSE/SSE2* 暫存器，傳遞異類向量匯總 (也稱為 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) 。</span><span class="sxs-lookup"><span data-stu-id="4871b-126">It can also pass heterogeneous vector aggregates (also known as [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) via *SSE/SSE2* registers if there is sufficient room.</span></span>

<span data-ttu-id="4871b-127">**適用于 ARM 上的 Windows**</span><span class="sxs-lookup"><span data-stu-id="4871b-127">**For Windows on ARM**</span></span>

<span data-ttu-id="4871b-128">ARM 上的 Windows & ARM64 支援將前四個 \_ \_ n128 值傳遞 ([**XMVECTOR**](xmvector-data-type.md)實例) 在註冊中。</span><span class="sxs-lookup"><span data-stu-id="4871b-128">The Windows on ARM & ARM64 supports passing the first four \_\_n128 values ([**XMVECTOR**](xmvector-data-type.md) instances) in-register.</span></span>

<span data-ttu-id="4871b-129">**DirectXMath 解決方案**</span><span class="sxs-lookup"><span data-stu-id="4871b-129">**DirectXMath solution**</span></span>

<span data-ttu-id="4871b-130">**FXMVECTOR**、 **GXMVECTOR**、 **HXMVECTOR** 和 **CXMVECTOR** 別名都支援下列慣例：</span><span class="sxs-lookup"><span data-stu-id="4871b-130">The **FXMVECTOR**, **GXMVECTOR**, **HXMVECTOR**, and **CXMVECTOR** aliases support these conventions:</span></span>

-   <span data-ttu-id="4871b-131">使用 **FXMVECTOR** 別名最多可傳遞給 [**XMVECTOR**](xmvector-data-type.md) 的前三個實例，做為函式的引數。</span><span class="sxs-lookup"><span data-stu-id="4871b-131">Use the **FXMVECTOR** alias to pass up to the first three instances of [**XMVECTOR**](xmvector-data-type.md) used as arguments to a function.</span></span>
-   <span data-ttu-id="4871b-132">使用 **GXMVECTOR** 別名，將做為引數之 [**XMVECTOR**](xmvector-data-type.md) 的第四個實例傳遞至函式。</span><span class="sxs-lookup"><span data-stu-id="4871b-132">Use the **GXMVECTOR** alias to pass the 4th instance of an [**XMVECTOR**](xmvector-data-type.md) used as an argument to a function.</span></span>
-   <span data-ttu-id="4871b-133">使用 **HXMVECTOR** 別名來傳遞 [**XMVECTOR**](xmvector-data-type.md) 的第5和第6個實例，做為函數的引數。</span><span class="sxs-lookup"><span data-stu-id="4871b-133">Use the **HXMVECTOR** alias to pass the 5th and 6th instances of an [**XMVECTOR**](xmvector-data-type.md) used as an argument to a function.</span></span> <span data-ttu-id="4871b-134">如需其他考慮的詳細資訊，請參閱 \_ \_ vectorcall 檔。</span><span class="sxs-lookup"><span data-stu-id="4871b-134">For info about additional considerations, see the \_\_vectorcall documentation.</span></span>
-   <span data-ttu-id="4871b-135">使用 **CXMVECTOR** 別名來傳遞任何進一步的 [**XMVECTOR**](xmvector-data-type.md) 實例，做為引數使用。</span><span class="sxs-lookup"><span data-stu-id="4871b-135">Use the **CXMVECTOR** alias to pass any further instances of [**XMVECTOR**](xmvector-data-type.md) used as arguments.</span></span>

> [!Note]  
> <span data-ttu-id="4871b-136">針對輸出參數，請一律使用 XMVECTOR \* 或 XMVECTOR&，並根據先前的輸入參數規則來忽略它們。</span><span class="sxs-lookup"><span data-stu-id="4871b-136">For output parameters, always use XMVECTOR\* or XMVECTOR& and ignore them with respect to the preceding rules for input parameters.</span></span>

 

<span data-ttu-id="4871b-137">由於 vectorcall 的限制 \_ \_ ，我們建議您不要針對 c + + 函式使用 **GXMVECTOR** 或 **HXMVECTOR** 。</span><span class="sxs-lookup"><span data-stu-id="4871b-137">Because of limitations with \_\_vectorcall, we recommend that you not use **GXMVECTOR** or **HXMVECTOR** for C++ constructors.</span></span> <span data-ttu-id="4871b-138">您只需針對前三個 [**XMVECTOR**](xmvector-data-type.md)值使用 **FXMVECTOR** ，然後將 **CXMVECTOR** 用於其餘部分。</span><span class="sxs-lookup"><span data-stu-id="4871b-138">Just use **FXMVECTOR** for the first three [**XMVECTOR**](xmvector-data-type.md) values, then use **CXMVECTOR** for the rest.</span></span>

<span data-ttu-id="4871b-139">**FXMMATRIX** 和 **CXMMATRIX** 別名有助於支援利用 vectorcall 傳遞的 HVA 引數 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4871b-139">The **FXMMATRIX** and **CXMMATRIX** aliases help support taking advantage of the HVA argument passing with \_\_vectorcall.</span></span>

-   <span data-ttu-id="4871b-140">使用 **FXMMATRIX** 別名，將第一個 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 做為引數傳遞至函式。</span><span class="sxs-lookup"><span data-stu-id="4871b-140">Use the **FXMMATRIX** alias to pass the first [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) as an argument to the function.</span></span> <span data-ttu-id="4871b-141">這假設您沒有兩個以上的 **FXMVECTOR** 引數，或兩個以上的 float、Double 或 **FXMVECTOR** 引數指向矩陣的 ' right '。</span><span class="sxs-lookup"><span data-stu-id="4871b-141">This assumes you don't have more than two **FXMVECTOR** arguments or more than two float, double, or **FXMVECTOR** arguments to the ‘right’ of the matrix.</span></span> <span data-ttu-id="4871b-142">如需其他考慮的詳細資訊，請參閱 \_ \_ vectorcall 檔。</span><span class="sxs-lookup"><span data-stu-id="4871b-142">For info about additional considerations, see the \_\_vectorcall documentation.</span></span>
-   <span data-ttu-id="4871b-143">請使用 **CXMMATRIX** 別名，否則為。</span><span class="sxs-lookup"><span data-stu-id="4871b-143">Use the **CXMMATRIX** alias otherwise.</span></span>

<span data-ttu-id="4871b-144">由於 vectorcall 的限制 \_ \_ ，我們建議您不要針對 c + + 函式使用 **FXMMATRIX** 。</span><span class="sxs-lookup"><span data-stu-id="4871b-144">Because of limitations with \_\_vectorcall, we recommend that you never use **FXMMATRIX** for C++ constructors.</span></span> <span data-ttu-id="4871b-145">只需使用 **CXMMATRIX**。</span><span class="sxs-lookup"><span data-stu-id="4871b-145">Just use **CXMMATRIX**.</span></span>

<span data-ttu-id="4871b-146">除了類型別名，您也必須使用 XM CALLCONV 注釋，以確定函式會根據 \_ 您的編譯器和架構，使用適當的呼叫慣例 (\_ \_ fastcall 和 \_ \_ vectorcall) 。</span><span class="sxs-lookup"><span data-stu-id="4871b-146">In addition to the type aliases, you must also use the XM\_CALLCONV annotation to make sure the function uses the appropriate calling convention (\_\_fastcall versus \_\_vectorcall) based on your compiler and architecture.</span></span> <span data-ttu-id="4871b-147">由於 vectorcall 的限制 \_ \_ ，我們建議您不要 \_ 針對 c + + 函式使用 XM CALLCONV。</span><span class="sxs-lookup"><span data-stu-id="4871b-147">Because of limitations with \_\_vectorcall, we recommend that you not use XM\_CALLCONV for C++ constructors.</span></span>

<span data-ttu-id="4871b-148">以下是說明此慣例的範例聲明：</span><span class="sxs-lookup"><span data-stu-id="4871b-148">The following are example declarations that illustrate this convention:</span></span>


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



<span data-ttu-id="4871b-149">為了支援這些呼叫慣例，這些類型的別名定義如下 (參數必須以傳值方式傳遞給編譯器，以將其視為內建的傳遞) ：</span><span class="sxs-lookup"><span data-stu-id="4871b-149">To support these calling conventions, these type aliases are defined as follows (parameters must be passed by value for the compiler to consider them for in-register passing):</span></span>

<span data-ttu-id="4871b-150">**適用于32位 Windows 應用程式**</span><span class="sxs-lookup"><span data-stu-id="4871b-150">**For 32-bit Windows apps**</span></span>

<span data-ttu-id="4871b-151">當您使用 \_ \_ fastcall 時：</span><span class="sxs-lookup"><span data-stu-id="4871b-151">When you use \_\_fastcall:</span></span>


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



<span data-ttu-id="4871b-152">當您使用 \_ \_ vectorcall 時：</span><span class="sxs-lookup"><span data-stu-id="4871b-152">When you use \_\_vectorcall:</span></span>


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



<span data-ttu-id="4871b-153">**適用于64位原生 Windows 應用程式**</span><span class="sxs-lookup"><span data-stu-id="4871b-153">**For 64-bit native Windows apps**</span></span>

<span data-ttu-id="4871b-154">當您使用 \_ \_ fastcall 時：</span><span class="sxs-lookup"><span data-stu-id="4871b-154">When you use \_\_fastcall:</span></span>


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



<span data-ttu-id="4871b-155">當您使用 \_ \_ vectorcall 時：</span><span class="sxs-lookup"><span data-stu-id="4871b-155">When you use \_\_vectorcall:</span></span>


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



<span data-ttu-id="4871b-156">**ARM 上的 Windows**</span><span class="sxs-lookup"><span data-stu-id="4871b-156">**Windows on ARM**</span></span>


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> <span data-ttu-id="4871b-157">雖然所有的函式都是以內嵌方式宣告，而且在許多情況下，編譯器不需要使用這些函式的呼叫慣例，但在某些情況下，編譯器可能會決定不內嵌函式，而在這些情況下，我們希望每個平臺都能有最佳的呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="4871b-157">While all the functions are declared inline and in many cases the compiler won't need to use calling conventions for these functions, there are cases where the compiler may decide it's more efficient to not inline the function and in these cases we want the best calling convention possible for each platform.</span></span>

 

## <a name="graphics-library-type-equivalence"></a><span data-ttu-id="4871b-158">圖形程式庫類型等價</span><span class="sxs-lookup"><span data-stu-id="4871b-158">Graphics Library Type Equivalence</span></span>

<span data-ttu-id="4871b-159">為了支援使用 DirectXMath 程式庫，許多 DirectXMath 程式庫類型和結構都相當於 **D3DDECLTYPE** 和 **D3DFORMAT** 類型的 Windows 實作為，以及 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 類型。</span><span class="sxs-lookup"><span data-stu-id="4871b-159">To support the use of the DirectXMath Library, many DirectXMath Library types and structures are equivalent to the Windows implementations of the **D3DDECLTYPE** and **D3DFORMAT** types, as well as the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) types.</span></span>

| <span data-ttu-id="4871b-160">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4871b-160">DirectXMath</span></span>                      | <span data-ttu-id="4871b-161">D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="4871b-161">D3DDECLTYPE</span></span>                                                                           | <span data-ttu-id="4871b-162">D3DFORMAT</span><span class="sxs-lookup"><span data-stu-id="4871b-162">D3DFORMAT</span></span>                                                     | <span data-ttu-id="4871b-163">DXGI \_ 格式</span><span class="sxs-lookup"><span data-stu-id="4871b-163">DXGI\_FORMAT</span></span>                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4871b-164">**XMBYTE2**</span><span class="sxs-lookup"><span data-stu-id="4871b-164">**XMBYTE2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | <span data-ttu-id="4871b-165">DXGI \_ 格式 \_ R8G8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="4871b-165">DXGI\_FORMAT\_R8G8\_SINT</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="4871b-166">**XMBYTE4**</span><span class="sxs-lookup"><span data-stu-id="4871b-166">**XMBYTE4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | <span data-ttu-id="4871b-167">D3DDECLTYPE \_ BYTE4 (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-167">D3DDECLTYPE\_BYTE4 (Xbox Only)</span></span>                                                        | <span data-ttu-id="4871b-168">D3DFMT \_ x8x8x8x8</span><span class="sxs-lookup"><span data-stu-id="4871b-168">D3DFMT\_x8x8x8x8</span></span>                                              | <span data-ttu-id="4871b-169">DXGI \_ 格式 \_ x8x8x8x8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="4871b-169">DXGI\_FORMAT\_x8x8x8x8\_SINT</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="4871b-170">**XMBYTEN2**</span><span class="sxs-lookup"><span data-stu-id="4871b-170">**XMBYTEN2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | <span data-ttu-id="4871b-171">D3DFMT \_ V8U8</span><span class="sxs-lookup"><span data-stu-id="4871b-171">D3DFMT\_V8U8</span></span>                                                  | <span data-ttu-id="4871b-172">DXGI \_ 格式 \_ R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-172">DXGI\_FORMAT\_R8G8\_SNORM</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="4871b-173">**XMBYTEN4**</span><span class="sxs-lookup"><span data-stu-id="4871b-173">**XMBYTEN4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | <span data-ttu-id="4871b-174">D3DDECLTYPE \_ BYTE4N (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-174">D3DDECLTYPE\_BYTE4N (Xbox Only)</span></span>                                                       | <span data-ttu-id="4871b-175">D3DFMT \_ x8x8x8x8</span><span class="sxs-lookup"><span data-stu-id="4871b-175">D3DFMT\_x8x8x8x8</span></span>                                              | <span data-ttu-id="4871b-176">DXGI \_ 格式 \_ x8x8x8x8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-176">DXGI\_FORMAT\_x8x8x8x8\_SNORM</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="4871b-177">**XMCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4871b-177">**XMCOLOR**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | <span data-ttu-id="4871b-178">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="4871b-178">D3DDECLTYPE\_D3DCOLOR</span></span>                                                                 | <span data-ttu-id="4871b-179">D3DFMT \_ A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="4871b-179">D3DFMT\_A8R8G8B8</span></span>                                              | <span data-ttu-id="4871b-180">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM (DXGI 1.1 +) </span><span class="sxs-lookup"><span data-stu-id="4871b-180">DXGI\_FORMAT\_B8G8R8A8\_UNORM (DXGI 1.1+)</span></span>                                                                                                                                                               |
| [<span data-ttu-id="4871b-181">**XMDEC4**</span><span class="sxs-lookup"><span data-stu-id="4871b-181">**XMDEC4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | <span data-ttu-id="4871b-182">D3DDECLTYPE \_ DEC4 (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-182">D3DDECLTYPE\_DEC4 (Xbox Only)</span></span>                                                         | <span data-ttu-id="4871b-183">D3DDECLTYPE \_ DEC3 (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-183">D3DDECLTYPE\_DEC3 (Xbox Only)</span></span>                                 |                                                                                                                                                                                                         |
| [<span data-ttu-id="4871b-184">**XMDECN4**</span><span class="sxs-lookup"><span data-stu-id="4871b-184">**XMDECN4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | <span data-ttu-id="4871b-185">D3DDECLTYPE \_ DEC4N (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-185">D3DDECLTYPE\_DEC4N (Xbox Only)</span></span>                                                        | <span data-ttu-id="4871b-186">D3DDECLTYPE \_ DEC3N (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-186">D3DDECLTYPE\_DEC3N (Xbox Only)</span></span>                                |                                                                                                                                                                                                         |
| [<span data-ttu-id="4871b-187">**XMFLOAT2**</span><span class="sxs-lookup"><span data-stu-id="4871b-187">**XMFLOAT2**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | <span data-ttu-id="4871b-188">D3DDECLTYPE \_ FLOAT2</span><span class="sxs-lookup"><span data-stu-id="4871b-188">D3DDECLTYPE\_FLOAT2</span></span>                                                                   | <span data-ttu-id="4871b-189">D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="4871b-189">D3DFMT\_G32R32F</span></span>                                               | <span data-ttu-id="4871b-190">DXGI \_ 格式 \_ R32G32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-190">DXGI\_FORMAT\_R32G32\_FLOAT</span></span>                                                                                                                                                                             |
| <span data-ttu-id="4871b-191">[**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4871b-191">[**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))</span></span>   | <span data-ttu-id="4871b-192">D3DDECLTYPE \_ FLOAT2</span><span class="sxs-lookup"><span data-stu-id="4871b-192">D3DDECLTYPE\_FLOAT2</span></span>                                                                   | <span data-ttu-id="4871b-193">D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="4871b-193">D3DFMT\_G32R32F</span></span>                                               | <span data-ttu-id="4871b-194">DXGI \_ 格式 \_ R32G32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-194">DXGI\_FORMAT\_R32G32\_FLOAT</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="4871b-195">**XMFLOAT3**</span><span class="sxs-lookup"><span data-stu-id="4871b-195">**XMFLOAT3**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | <span data-ttu-id="4871b-196">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="4871b-196">D3DDECLTYPE\_FLOAT3</span></span>                                                                   |                                                               | <span data-ttu-id="4871b-197">DXGI \_ 格式 \_ R32G32B32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-197">DXGI\_FORMAT\_R32G32B32\_FLOAT</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="4871b-198">**XMFLOAT3A**</span><span class="sxs-lookup"><span data-stu-id="4871b-198">**XMFLOAT3A**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | <span data-ttu-id="4871b-199">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="4871b-199">D3DDECLTYPE\_FLOAT3</span></span>                                                                   |                                                               | <span data-ttu-id="4871b-200">DXGI \_ 格式 \_ R32G32B32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-200">DXGI\_FORMAT\_R32G32B32\_FLOAT</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="4871b-201">**XMFLOAT3PK**</span><span class="sxs-lookup"><span data-stu-id="4871b-201">**XMFLOAT3PK**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | <span data-ttu-id="4871b-202">DXGI \_ 格式 \_ R11G11B10 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-202">DXGI\_FORMAT\_R11G11B10\_FLOAT</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="4871b-203">**XMFLOAT3SE**</span><span class="sxs-lookup"><span data-stu-id="4871b-203">**XMFLOAT3SE**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | <span data-ttu-id="4871b-204">DXGI \_ 格式 \_ R9G9B9E5 \_ SHAREDEXP</span><span class="sxs-lookup"><span data-stu-id="4871b-204">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="4871b-205">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="4871b-205">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | <span data-ttu-id="4871b-206">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="4871b-206">D3DDECLTYPE\_FLOAT4</span></span>                                                                   | <span data-ttu-id="4871b-207">D3DFMT \_ A32B32G32R32F</span><span class="sxs-lookup"><span data-stu-id="4871b-207">D3DFMT\_A32B32G32R32F</span></span>                                         | <span data-ttu-id="4871b-208">DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-208">DXGI\_FORMAT\_R32G32B32A32\_FLOAT</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="4871b-209">**XMFLOAT4A**</span><span class="sxs-lookup"><span data-stu-id="4871b-209">**XMFLOAT4A**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | <span data-ttu-id="4871b-210">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="4871b-210">D3DDECLTYPE\_FLOAT4</span></span>                                                                   | <span data-ttu-id="4871b-211">D3DFMT \_ A32B32G32R32F</span><span class="sxs-lookup"><span data-stu-id="4871b-211">D3DFMT\_A32B32G32R32F</span></span>                                         | <span data-ttu-id="4871b-212">DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-212">DXGI\_FORMAT\_R32G32B32A32\_FLOAT</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="4871b-213">**XMHALF2**</span><span class="sxs-lookup"><span data-stu-id="4871b-213">**XMHALF2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | <span data-ttu-id="4871b-214">D3DDECLTYPE \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="4871b-214">D3DDECLTYPE\_FLOAT16\_2</span></span>                                                               | <span data-ttu-id="4871b-215">D3DFMT \_ G16R16F</span><span class="sxs-lookup"><span data-stu-id="4871b-215">D3DFMT\_G16R16F</span></span>                                               | <span data-ttu-id="4871b-216">DXGI \_ 格式 \_ R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-216">DXGI\_FORMAT\_R16G16\_FLOAT</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="4871b-217">**XMHALF4**</span><span class="sxs-lookup"><span data-stu-id="4871b-217">**XMHALF4**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | <span data-ttu-id="4871b-218">D3DDECLTYPE \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="4871b-218">D3DDECLTYPE\_FLOAT16\_4</span></span>                                                               | <span data-ttu-id="4871b-219">D3DFMT \_ A16B16G16R16F</span><span class="sxs-lookup"><span data-stu-id="4871b-219">D3DFMT\_A16B16G16R16F</span></span>                                         | <span data-ttu-id="4871b-220">DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="4871b-220">DXGI\_FORMAT\_R16G16B16A16\_FLOAT</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="4871b-221">**XMINT2**</span><span class="sxs-lookup"><span data-stu-id="4871b-221">**XMINT2**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | <span data-ttu-id="4871b-222">DXGI \_ 格式 \_ R32G32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="4871b-222">DXGI\_FORMAT\_R32G32\_SINT</span></span>                                                                                                                                                                              |
| [<span data-ttu-id="4871b-223">**XMINT3**</span><span class="sxs-lookup"><span data-stu-id="4871b-223">**XMINT3**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | <span data-ttu-id="4871b-224">DXGI \_ 格式 \_ R32G32B32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="4871b-224">DXGI\_FORMAT\_R32G32B32\_SINT</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="4871b-225">**XMINT4**</span><span class="sxs-lookup"><span data-stu-id="4871b-225">**XMINT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | <span data-ttu-id="4871b-226">DXGI \_ 格式 \_ R32G32B32A32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="4871b-226">DXGI\_FORMAT\_R32G32B32A32\_SINT</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="4871b-227">**XMSHORT2**</span><span class="sxs-lookup"><span data-stu-id="4871b-227">**XMSHORT2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | <span data-ttu-id="4871b-228">D3DDECLTYPE \_ SHORT2</span><span class="sxs-lookup"><span data-stu-id="4871b-228">D3DDECLTYPE\_SHORT2</span></span>                                                                   | <span data-ttu-id="4871b-229">D3DFMT \_ V16U16</span><span class="sxs-lookup"><span data-stu-id="4871b-229">D3DFMT\_V16U16</span></span>                                                | <span data-ttu-id="4871b-230">DXGI \_ 格式 \_ R16G16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="4871b-230">DXGI\_FORMAT\_R16G16\_SINT</span></span>                                                                                                                                                                              |
| [<span data-ttu-id="4871b-231">**XMSHORTN2**</span><span class="sxs-lookup"><span data-stu-id="4871b-231">**XMSHORTN2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | <span data-ttu-id="4871b-232">D3DDECLTYPE \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="4871b-232">D3DDECLTYPE\_SHORT2N</span></span>                                                                  | <span data-ttu-id="4871b-233">D3DFMT \_ V16U16</span><span class="sxs-lookup"><span data-stu-id="4871b-233">D3DFMT\_V16U16</span></span>                                                | <span data-ttu-id="4871b-234">DXGI \_ 格式 \_ R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-234">DXGI\_FORMAT\_R16G16\_SNORM</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="4871b-235">**XMSHORT4**</span><span class="sxs-lookup"><span data-stu-id="4871b-235">**XMSHORT4**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | <span data-ttu-id="4871b-236">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="4871b-236">D3DDECLTYPE\_SHORT4</span></span>                                                                   | <span data-ttu-id="4871b-237">D3DFMT \_ x16x16x16x16</span><span class="sxs-lookup"><span data-stu-id="4871b-237">D3DFMT\_x16x16x16x16</span></span>                                          | <span data-ttu-id="4871b-238">DXGI \_ 格式 \_ R16G16B16A16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="4871b-238">DXGI\_FORMAT\_R16G16B16A16\_SINT</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="4871b-239">**XMSHORTN4**</span><span class="sxs-lookup"><span data-stu-id="4871b-239">**XMSHORTN4**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | <span data-ttu-id="4871b-240">D3DDECLTYPE \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="4871b-240">D3DDECLTYPE\_SHORT4N</span></span>                                                                  | <span data-ttu-id="4871b-241">D3DFMT \_ x16x16x16x16</span><span class="sxs-lookup"><span data-stu-id="4871b-241">D3DFMT\_x16x16x16x16</span></span>                                          | <span data-ttu-id="4871b-242">DXGI \_ 格式 \_ R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-242">DXGI\_FORMAT\_R16G16B16A16\_SNORM</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="4871b-243">**XMUBYTE2**</span><span class="sxs-lookup"><span data-stu-id="4871b-243">**XMUBYTE2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | <span data-ttu-id="4871b-244">DXGI \_ 格式 \_ R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4871b-244">DXGI\_FORMAT\_R8G8\_UINT</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="4871b-245">**XMUBYTEN2**</span><span class="sxs-lookup"><span data-stu-id="4871b-245">**XMUBYTEN2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | <span data-ttu-id="4871b-246">D3DFMT \_ A8P8、D3DFMT \_ A8L8</span><span class="sxs-lookup"><span data-stu-id="4871b-246">D3DFMT\_A8P8, D3DFMT\_A8L8</span></span>                                    | <span data-ttu-id="4871b-247">DXGI \_ 格式 \_ R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-247">DXGI\_FORMAT\_R8G8\_UNORM</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="4871b-248">**XMUINT2**</span><span class="sxs-lookup"><span data-stu-id="4871b-248">**XMUINT2**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | <span data-ttu-id="4871b-249">DXGI \_ 格式 \_ R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4871b-249">DXGI\_FORMAT\_R32G32\_UINT</span></span>                                                                                                                                                                              |
| [<span data-ttu-id="4871b-250">**XMUINT3**</span><span class="sxs-lookup"><span data-stu-id="4871b-250">**XMUINT3**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | <span data-ttu-id="4871b-251">DXGI \_ 格式 \_ R32G32B32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4871b-251">DXGI\_FORMAT\_R32G32B32\_UINT</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="4871b-252">**XMUINT4**</span><span class="sxs-lookup"><span data-stu-id="4871b-252">**XMUINT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | <span data-ttu-id="4871b-253">DXGI \_ 格式 \_ R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4871b-253">DXGI\_FORMAT\_R32G32B32A32\_UINT</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="4871b-254">**XMU555**</span><span class="sxs-lookup"><span data-stu-id="4871b-254">**XMU555**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | <span data-ttu-id="4871b-255">D3DFMT \_ X1R5G5B5、D3DFMT \_ A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="4871b-255">D3DFMT\_X1R5G5B5, D3DFMT\_A1R5G5B5</span></span>                            | <span data-ttu-id="4871b-256">DXGI \_ 格式 \_ B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-256">DXGI\_FORMAT\_B5G5R5A1\_UNORM</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="4871b-257">**XMU565**</span><span class="sxs-lookup"><span data-stu-id="4871b-257">**XMU565**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | <span data-ttu-id="4871b-258">D3DFMT \_ R5G6B5</span><span class="sxs-lookup"><span data-stu-id="4871b-258">D3DFMT\_R5G6B5</span></span>                                                | <span data-ttu-id="4871b-259">DXGI \_ 格式 \_ B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-259">DXGI\_FORMAT\_B5G6R5\_UNORM</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="4871b-260">**XMUBYTE4**</span><span class="sxs-lookup"><span data-stu-id="4871b-260">**XMUBYTE4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | <span data-ttu-id="4871b-261">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="4871b-261">D3DDECLTYPE\_UBYTE4</span></span>                                                                   | <span data-ttu-id="4871b-262">D3DFMT \_ x8x8x8x8</span><span class="sxs-lookup"><span data-stu-id="4871b-262">D3DFMT\_x8x8x8x8</span></span>                                              | <span data-ttu-id="4871b-263">DXGI \_ 格式 \_ x8x8x8x8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4871b-263">DXGI\_FORMAT\_x8x8x8x8\_UINT</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="4871b-264">**XMUBYTEN4**</span><span class="sxs-lookup"><span data-stu-id="4871b-264">**XMUBYTEN4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | <span data-ttu-id="4871b-265">D3DDECLTYPE \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="4871b-265">D3DDECLTYPE\_UBYTE4N</span></span>                                                                  | <span data-ttu-id="4871b-266">D3DFMT \_ x8x8x8x8</span><span class="sxs-lookup"><span data-stu-id="4871b-266">D3DFMT\_x8x8x8x8</span></span>                                              | <span data-ttu-id="4871b-267">DXGI \_ 格式 \_ x8x8x8x8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-267">DXGI\_FORMAT\_x8x8x8x8\_UNORM</span></span><br/> <span data-ttu-id="4871b-268">DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM (使用 [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) 和 [**XMStoreUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)。 ) </span><span class="sxs-lookup"><span data-stu-id="4871b-268">DXGI\_FORMAT\_R10G10B10\_XR\_BIAS\_A2\_UNORM (Use [**XMLoadUDecN4\_XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) and [**XMStoreUDecN4\_XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr).)</span></span><br/> |
| [<span data-ttu-id="4871b-269">**XMUDEC4**</span><span class="sxs-lookup"><span data-stu-id="4871b-269">**XMUDEC4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | <span data-ttu-id="4871b-270">D3DDECLTYPE \_ UDEC4 (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-270">D3DDECLTYPE\_UDEC4 (Xbox Only)</span></span><br/> <span data-ttu-id="4871b-271">D3DDECLTYPE \_ UDEC3 (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-271">D3DDECLTYPE\_UDEC3 (Xbox Only)</span></span><br/>   | <span data-ttu-id="4871b-272">D3DFMT \_ A2R10G10B10</span><span class="sxs-lookup"><span data-stu-id="4871b-272">D3DFMT\_A2R10G10B10</span></span><br/> <span data-ttu-id="4871b-273">D3DFMT \_ A2B10G10R10</span><span class="sxs-lookup"><span data-stu-id="4871b-273">D3DFMT\_A2B10G10R10</span></span><br/> | <span data-ttu-id="4871b-274">DXGI \_ 格式 \_ R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4871b-274">DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="4871b-275">**XMUDECN4**</span><span class="sxs-lookup"><span data-stu-id="4871b-275">**XMUDECN4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | <span data-ttu-id="4871b-276">D3DDECLTYPE \_ UDEC4N (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-276">D3DDECLTYPE\_UDEC4N (Xbox Only)</span></span><br/> <span data-ttu-id="4871b-277">D3DDECLTYPE \_ UDEC3N (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-277">D3DDECLTYPE\_UDEC3N (Xbox Only)</span></span><br/> | <span data-ttu-id="4871b-278">D3DFMT \_ A2R10G10B10</span><span class="sxs-lookup"><span data-stu-id="4871b-278">D3DFMT\_A2R10G10B10</span></span><br/> <span data-ttu-id="4871b-279">D3DFMT \_ A2B10G10R10</span><span class="sxs-lookup"><span data-stu-id="4871b-279">D3DFMT\_A2B10G10R10</span></span><br/> | <span data-ttu-id="4871b-280">DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-280">DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="4871b-281">**XMUNIBBLE4**</span><span class="sxs-lookup"><span data-stu-id="4871b-281">**XMUNIBBLE4**</span></span>](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | <span data-ttu-id="4871b-282">D3DFMT \_ A4R4G4B4、D3DFMT \_ X4R4G4B4</span><span class="sxs-lookup"><span data-stu-id="4871b-282">D3DFMT\_A4R4G4B4, D3DFMT\_X4R4G4B4</span></span>                            | <span data-ttu-id="4871b-283">DXGI \_ 格式 \_ B4G4R4A4 \_ UNORM (DXGI 1.2 +) </span><span class="sxs-lookup"><span data-stu-id="4871b-283">DXGI\_FORMAT\_B4G4R4A4\_UNORM (DXGI 1.2+)</span></span>                                                                                                                                                               |
| [<span data-ttu-id="4871b-284">**XMUSHORT2**</span><span class="sxs-lookup"><span data-stu-id="4871b-284">**XMUSHORT2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | <span data-ttu-id="4871b-285">D3DDECLTYPE \_ USHORT2</span><span class="sxs-lookup"><span data-stu-id="4871b-285">D3DDECLTYPE\_USHORT2</span></span>                                                                  | <span data-ttu-id="4871b-286">D3DFMT \_ G16R16</span><span class="sxs-lookup"><span data-stu-id="4871b-286">D3DFMT\_G16R16</span></span>                                                | <span data-ttu-id="4871b-287">DXGI \_ 格式 \_ R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4871b-287">DXGI\_FORMAT\_R16G16\_UINT</span></span>                                                                                                                                                                              |
| [<span data-ttu-id="4871b-288">**XMUSHORTN2**</span><span class="sxs-lookup"><span data-stu-id="4871b-288">**XMUSHORTN2**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | <span data-ttu-id="4871b-289">D3DDECLTYPE \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="4871b-289">D3DDECLTYPE\_USHORT2N</span></span>                                                                 | <span data-ttu-id="4871b-290">D3DFMT \_ G16R16</span><span class="sxs-lookup"><span data-stu-id="4871b-290">D3DFMT\_G16R16</span></span>                                                | <span data-ttu-id="4871b-291">DXGI \_ 格式 \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-291">DXGI\_FORMAT\_R16G16\_UNORM</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="4871b-292">**XMUSHORT4**</span><span class="sxs-lookup"><span data-stu-id="4871b-292">**XMUSHORT4**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | <span data-ttu-id="4871b-293">D3DDECLTYPE \_ USHORT4 (僅限 Xbox) </span><span class="sxs-lookup"><span data-stu-id="4871b-293">D3DDECLTYPE\_USHORT4 (Xbox Only)</span></span>                                                      | <span data-ttu-id="4871b-294">D3DFMT \_ x16x16x16x16</span><span class="sxs-lookup"><span data-stu-id="4871b-294">D3DFMT\_x16x16x16x16</span></span>                                          | <span data-ttu-id="4871b-295">DXGI \_ 格式 \_ R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="4871b-295">DXGI\_FORMAT\_R16G16B16A16\_UINT</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="4871b-296">**XMUSHORTN4**</span><span class="sxs-lookup"><span data-stu-id="4871b-296">**XMUSHORTN4**</span></span>](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | <span data-ttu-id="4871b-297">D3DDECLTYPE \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="4871b-297">D3DDECLTYPE\_USHORT4N</span></span>                                                                 | <span data-ttu-id="4871b-298">D3DFMT \_ x16x16x16x16</span><span class="sxs-lookup"><span data-stu-id="4871b-298">D3DFMT\_x16x16x16x16</span></span>                                          | <span data-ttu-id="4871b-299">DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="4871b-299">DXGI\_FORMAT\_R16G16B16A16\_UNORM</span></span>                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a><span data-ttu-id="4871b-300">DirectXMath 程式庫中的全域常數</span><span class="sxs-lookup"><span data-stu-id="4871b-300">Global Constants in the DirectXMath Library</span></span>

<span data-ttu-id="4871b-301">為了減少資料區段的大小，DirectXMath 程式庫會使用 [XMGLOBALCONST](xmglobalconst.md) 宏來利用其實值中的一些全域內部常數。</span><span class="sxs-lookup"><span data-stu-id="4871b-301">To reduce the size of the data segment, the DirectXMath Library uses the [XMGLOBALCONST](xmglobalconst.md) macro to make use of a number of global internal constants in its implementation.</span></span> <span data-ttu-id="4871b-302">依照慣例，這類內部全域常數前面會加上 **g \_ XM**。</span><span class="sxs-lookup"><span data-stu-id="4871b-302">By convention, such internal global constants are prefixed by **g\_XM**.</span></span> <span data-ttu-id="4871b-303">一般而言，它們是下列其中一種類型： [**XMVECTORU32**](xmvectoru32-data-type.md)、 [**XMVECTORF32**](xmvectorf32-data-type.md)或 **XMVECTORI32**。</span><span class="sxs-lookup"><span data-stu-id="4871b-303">Typically, they are one of the following types: [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORF32**](xmvectorf32-data-type.md), or **XMVECTORI32**.</span></span>

<span data-ttu-id="4871b-304">這些內部全域常數可能會在未來的 DirectXMath 程式庫修訂中變更。</span><span class="sxs-lookup"><span data-stu-id="4871b-304">These internal global constants are subject to change in future revisions of the DirectXMath Library.</span></span> <span data-ttu-id="4871b-305">使用可封裝常數的公用函式（可能的話），而不是直接使用 **g \_ XM** 全域值。</span><span class="sxs-lookup"><span data-stu-id="4871b-305">Use public functions that encapsulate the constants when possible rather than direct use of **g\_XM** global values.</span></span> <span data-ttu-id="4871b-306">您也可以使用 [XMGLOBALCONST](xmglobalconst.md)宣告您自己的全域常數。</span><span class="sxs-lookup"><span data-stu-id="4871b-306">You can also declare your own global constants using [XMGLOBALCONST](xmglobalconst.md).</span></span>

## <a name="windows-sse-versus-sse2"></a><span data-ttu-id="4871b-307">Windows SSE 與 SSE2</span><span class="sxs-lookup"><span data-stu-id="4871b-307">Windows SSE versus SSE2</span></span>

<span data-ttu-id="4871b-308">SSE 指令集僅提供單精確度浮點向量的支援。</span><span class="sxs-lookup"><span data-stu-id="4871b-308">The SSE instruction set provides support only for single-precision floating-point vectors.</span></span> <span data-ttu-id="4871b-309">DirectXMath 必須利用 SSE2 指令集來提供整數向量支援。</span><span class="sxs-lookup"><span data-stu-id="4871b-309">DirectXMath must make use of the SSE2 instruction set to provide integer vector support.</span></span> <span data-ttu-id="4871b-310">自 Pentium 4、所有 AMD K8 和更新版本的處理器，以及所有 x64 支援的處理器推出之後，所有 Intel 處理器都支援 SSE2。</span><span class="sxs-lookup"><span data-stu-id="4871b-310">SSE2 is supported by all Intel processors since the introduction of the Pentium 4, all AMD K8 and later processors, and all x64-capable processors.</span></span>

> [!Note]  
> <span data-ttu-id="4871b-311">X86 或更新版本的 Windows 8 需要支援 SSE2。</span><span class="sxs-lookup"><span data-stu-id="4871b-311">Windows 8 for x86 or later requires support for SSE2.</span></span> <span data-ttu-id="4871b-312">所有版本的 Windows x64 都需要 SSE2 的支援。</span><span class="sxs-lookup"><span data-stu-id="4871b-312">All versions of Windows x64 require support for SSE2.</span></span> <span data-ttu-id="4871b-313">ARM/ARM64 上的 Windows 需要 ARM \_ 霓虹燈。</span><span class="sxs-lookup"><span data-stu-id="4871b-313">Windows on ARM / ARM64 requires ARM\_NEON.</span></span>

 

## <a name="routine-variants"></a><span data-ttu-id="4871b-314">常式變數</span><span class="sxs-lookup"><span data-stu-id="4871b-314">Routine Variants</span></span>

<span data-ttu-id="4871b-315">有數種 DirectXMath 函式可讓您更輕鬆地執行您的工作：</span><span class="sxs-lookup"><span data-stu-id="4871b-315">There are several variants of DirectXMath functions that make it easier to do your work:</span></span>

-   <span data-ttu-id="4871b-316">比較函式，根據較少量的向量比較作業來建立複雜的條件式分支。</span><span class="sxs-lookup"><span data-stu-id="4871b-316">Comparison functions to create complicated conditional branching based on a smaller number of vector comparison operations.</span></span> <span data-ttu-id="4871b-317">這些函式的名稱會以 "R" 結尾，例如 XMVector3InBoundsR。</span><span class="sxs-lookup"><span data-stu-id="4871b-317">The name of these functions end in "R" such as XMVector3InBoundsR.</span></span> <span data-ttu-id="4871b-318">函數會以 UINT 傳回值或 UINT out 參數傳回比較記錄。</span><span class="sxs-lookup"><span data-stu-id="4871b-318">The functions return a comparison record as a UINT return value, or as a UINT out parameter.</span></span> <span data-ttu-id="4871b-319">您可以使用 **XMComparision \*** 宏來測試值。</span><span class="sxs-lookup"><span data-stu-id="4871b-319">You can use the **XMComparision\*** macros to test the value.</span></span>
-   <span data-ttu-id="4871b-320">在較大型向量陣列上執行批次樣式作業的批次函數。</span><span class="sxs-lookup"><span data-stu-id="4871b-320">Batch functions for performing batch-style operations on larger vector arrays.</span></span> <span data-ttu-id="4871b-321">這些函式的名稱會以 "Stream" 結尾，例如 [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)。</span><span class="sxs-lookup"><span data-stu-id="4871b-321">The name of these functions end in "Stream" such as [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream).</span></span> <span data-ttu-id="4871b-322">這些函式會在輸入的陣列上操作，而且會產生輸出的陣列。</span><span class="sxs-lookup"><span data-stu-id="4871b-322">The functions operate on an array of inputs, and they generate an array of outputs.</span></span> <span data-ttu-id="4871b-323">通常，它們會採用輸入和輸出 stride。</span><span class="sxs-lookup"><span data-stu-id="4871b-323">Typically, they take an input and output stride.</span></span>
-   <span data-ttu-id="4871b-324">評估函式，以執行更快的估計，而不是較慢且更精確的結果。</span><span class="sxs-lookup"><span data-stu-id="4871b-324">Estimation functions that implement a faster estimation instead of a slower, more accurate result.</span></span> <span data-ttu-id="4871b-325">這些函式的名稱結尾是 "Est"，例如 [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest)。</span><span class="sxs-lookup"><span data-stu-id="4871b-325">The name of these functions end in "Est" such as [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest).</span></span> <span data-ttu-id="4871b-326">使用估計的品質和效能影響會因平臺而異，但我們建議您針對效能相關的程式碼使用估計變異。</span><span class="sxs-lookup"><span data-stu-id="4871b-326">The quality and performance impact of using estimation varies from platform to platform, but we recommend that you use estimation variants for performance-sensitive code.</span></span>

## <a name="platform-inconsistencies"></a><span data-ttu-id="4871b-327">平臺不一致</span><span class="sxs-lookup"><span data-stu-id="4871b-327">Platform Inconsistencies</span></span>

<span data-ttu-id="4871b-328">DirectXMath 程式庫是要用於效能相關的圖形應用程式和遊戲中。</span><span class="sxs-lookup"><span data-stu-id="4871b-328">The DirectXMath library is intended for use in performance-sensitive graphics applications and games.</span></span> <span data-ttu-id="4871b-329">因此，其設計目的是為了在所有支援的平臺上進行正常處理的最佳速度。</span><span class="sxs-lookup"><span data-stu-id="4871b-329">Therefore, the implementation is designed for optimal speed doing normal processing on all supported platforms.</span></span> <span data-ttu-id="4871b-330">界限條件的結果，尤其是產生浮點數特殊的結果，可能會因目標而異。</span><span class="sxs-lookup"><span data-stu-id="4871b-330">Results at boundary-conditions, particularly those that generate floating-point specials, are likely to vary from target to target.</span></span> <span data-ttu-id="4871b-331">此行為也將取決於其他執行時間設定，例如 Windows 32 位的非內建函式目標的 x87 控制字組，或 Windows 32 位和64位的 SSE 控制字組。</span><span class="sxs-lookup"><span data-stu-id="4871b-331">This behavior will also depend on other run-time settings, such as the x87 control word for the Windows 32-bit no-intrinsics target or the SSE control word for both Windows 32-bit and 64-bit.</span></span> <span data-ttu-id="4871b-332">此外，不同 CPU 廠商之間的界限條件之間會有差異。</span><span class="sxs-lookup"><span data-stu-id="4871b-332">Furthermore, there will be differences in boundary-conditions between various CPU vendors.</span></span>

<span data-ttu-id="4871b-333">請勿在科學或其他應用程式中使用 DirectXMath，其中數位精確度是最重要的。</span><span class="sxs-lookup"><span data-stu-id="4871b-333">Don't use DirectXMath in scientific or other applications where numerical accuracy is paramount.</span></span> <span data-ttu-id="4871b-334">此外，這項限制會反映在缺少雙或其他延伸精確度計算的支援。</span><span class="sxs-lookup"><span data-stu-id="4871b-334">Also, this limitation is reflected in the lack of support for double or other extended precision computations.</span></span>

> [!Note]  
> <span data-ttu-id="4871b-335">如果沒有任何內建純量純量 \_ \_ \_ \_ 程式碼路徑，通常會針對合規性撰寫，而不是效能。</span><span class="sxs-lookup"><span data-stu-id="4871b-335">The \_XM\_NO\_INTRINSICS\_ scalar code paths generally are written for compliance, not performance.</span></span> <span data-ttu-id="4871b-336">它們的界限條件結果也會不同。</span><span class="sxs-lookup"><span data-stu-id="4871b-336">Their boundary-condition results also will vary.</span></span>

 

## <a name="platform-specific-extensions"></a><span data-ttu-id="4871b-337">平臺特定的擴充功能</span><span class="sxs-lookup"><span data-stu-id="4871b-337">Platform-specific Extensions</span></span>

<span data-ttu-id="4871b-338">DirectXMath 程式庫旨在簡化 c + + SIMD 程式設計，為 x86、x64 和 Windows RT 平臺提供絕佳的支援，其使用廣泛支援的內建指示 (SSE2 和 ARM-霓虹燈) 。</span><span class="sxs-lookup"><span data-stu-id="4871b-338">The DirectXMath library is intended to simplify C++ SIMD programming providing excellent support for x86, x64, and Windows RT platforms using broadly supported intrinsics instructions (SSE2 and ARM-NEON).</span></span>

<span data-ttu-id="4871b-339">不過，在某些情況下，平臺特定的指示可能會有所説明。</span><span class="sxs-lookup"><span data-stu-id="4871b-339">There are times, however, when platform-specific instructions may prove beneficial.</span></span> <span data-ttu-id="4871b-340">由於 DirectXMath 的實現方式，在許多情況下，直接在標準編譯器支援的內建語句中使用 DirectXMath 類型，以及使用 DirectXMath 作為不支援擴充指令之平臺的回溯路徑是很簡單的。</span><span class="sxs-lookup"><span data-stu-id="4871b-340">Due to the way DirectXMath is implemented, in many cases it is trivial to use DirectXMath types directly in standard compiler-supported intrinsics statements, and to use DirectXMath as the fallback path for platforms that don't support the extended instruction.</span></span>

<span data-ttu-id="4871b-341">例如，以下是利用 SSE 4.1 點產品指令的簡化範例。</span><span class="sxs-lookup"><span data-stu-id="4871b-341">For example, here is a simplified example of leveraging the SSE 4.1 dot-product instruction.</span></span> <span data-ttu-id="4871b-342">請注意，您必須明確防護程式碼路徑，以避免在執行時間產生不正確指令例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4871b-342">Note that you must explicitly guard the code-path to avoid generating invalid instruction exceptions at run time.</span></span> <span data-ttu-id="4871b-343">確定程式碼路徑有足夠的工作，以證明分支的額外成本、維護多個程式碼路徑的複雜性等等。</span><span class="sxs-lookup"><span data-stu-id="4871b-343">Ensure the code paths do significant enough work to justify the additional cost of branching, complexity of maintaining multiple code-paths, and so on.</span></span>


```
#include <Windows.h>
#include <stdio.h>

#include <DirectXMath.h>

#include <intrin.h>
#include <smmintrin.h>

using namespace DirectX;

bool g_bSSE41 = false;

void DetectCPUFeatures()
{
#ifndef _M_ARM
   // See __cpuid documentation on MSDN for more information

   int CPUInfo[4] = {-1};
#if defined(__clang__) || defined(__GNUC__)
   __cpuid(0, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
   __cpuid(CPUInfo, 0);
#endif

   if ( CPUInfo[0] >= 1 )
   {
#if defined(__clang__) || defined(__GNUC__)
        __cpuid(1, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
        __cpuid(CPUInfo, 1);
#endif

       if ( CPUInfo[2] & 0x80000 )
           g_bSSE41 = true;
   }
#endif
}

int main()
{
   if ( !XMVerifyCPUSupport() )
       return -1;

   DetectCPUFeatures();

   ...

   XMVECTORF32 v1 = { 1.f, 2.f, 3.f, 4.f };
   XMVECTORF32 v2 = { 5.f, 6.f, 7.f, 8.f };

   XMVECTOR r2, r3, r4;

   if ( g_bSSE41 )
   {
#ifndef _M_ARM
       r2 = _mm_dp_ps( v1, v2, 0x3f );
       r3 = _mm_dp_ps( v1, v2, 0x7f );
       r4 = _mm_dp_ps( v1, v2, 0xff );
#endif
   }
   else
   {
       r2 = XMVector2Dot( v1, v2 );
       r3 = XMVector3Dot( v1, v2 );
       r4 = XMVector4Dot( v1, v2 );
   }

   ...

   return 0;
}
```



<span data-ttu-id="4871b-344">如需平臺特定擴充功能的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="4871b-344">For more info about platform-specific extensions, see:</span></span>

<dl>

[<span data-ttu-id="4871b-345">DirectXMath： SSE、SSE2 和 ARM-霓虹燈</span><span class="sxs-lookup"><span data-stu-id="4871b-345">DirectXMath: SSE, SSE2, and ARM-NEON</span></span>](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[<span data-ttu-id="4871b-346">DirectXMath： SSE3 和 SSSE3</span><span class="sxs-lookup"><span data-stu-id="4871b-346">DirectXMath: SSE3 and SSSE3</span></span>](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[<span data-ttu-id="4871b-347">DirectXMath： SSE 4.1 和 SSE 4。2</span><span class="sxs-lookup"><span data-stu-id="4871b-347">DirectXMath: SSE4.1 and SSE4.2</span></span>](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[<span data-ttu-id="4871b-348">DirectXMath： AVX</span><span class="sxs-lookup"><span data-stu-id="4871b-348">DirectXMath: AVX</span></span>](https://walbourn.github.io/directxmath-avx/)  
[<span data-ttu-id="4871b-349">DirectXMath： F16C 和 FMA</span><span class="sxs-lookup"><span data-stu-id="4871b-349">DirectXMath: F16C and FMA</span></span>](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[<span data-ttu-id="4871b-350">DirectXMath： AVX2</span><span class="sxs-lookup"><span data-stu-id="4871b-350">DirectXMath: AVX2</span></span>](https://walbourn.github.io/directxmath-avx2/)  
[<span data-ttu-id="4871b-351">DirectXMath： ARM64</span><span class="sxs-lookup"><span data-stu-id="4871b-351">DirectXMath: ARM64</span></span>](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="4871b-352">相關主題</span><span class="sxs-lookup"><span data-stu-id="4871b-352">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4871b-353">DirectXMath 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="4871b-353">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
