---
description: 本主題說明 DirectXMath 程式庫的優化考慮和策略。
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: 使用 DirectXMath 程式庫進行程式碼優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263434b5e7295f630f284517299cec036b33b064d35dc5085a83d67c8244366a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984718"
---
# <a name="code-optimization-with-the-directxmath-library"></a>使用 DirectXMath 程式庫進行程式碼優化

本主題說明 DirectXMath 程式庫的優化考慮和策略。

-   [謹慎使用存取子](#use-accessors-sparingly)
-   [使用正確的編譯設定](#use-correct-compilation-settings)
-   [適當時使用 Est 函數](#use-est-functions-when-appropriate)
-   [使用對齊的資料類型和作業](#use-aligned-data-types-and-operations)
-   [適當地對齊配置](#properly-align-allocations)
-   [盡可能避免運算子多載](#avoid-operator-overloads-when-possible)
-   [非正規數](#denormals)
-   [利用整數浮點數類雙重特性](#take-advantage-of-the-integer-floating-point-duality)
-   [偏好範本表單](#prefer-template-forms)
-   [搭配使用 DirectXMath 與 Direct3D](#using-directxmath-with-direct3d)
-   [相關主題](#related-topics)

## <a name="use-accessors-sparingly"></a>謹慎使用存取子

以向量為基礎的作業會使用 SIMD 指令集，而這些指令集會利用特殊暫存器。 存取個別元件需要從 SIMD 暫存器移動到純量專案，然後再重新進行。

可能的話，您可以更有效率地一次初始化 [**XMVECTOR**](xmvector-data-type.md) 的所有元件，而不是使用一連串個別的向量存取子。

## <a name="use-correct-compilation-settings"></a>使用正確的編譯設定

針對 Windows x86 目標，請啟用/arch： SSE2。 針對所有 Windows 目標，啟用/fp： fast。

根據預設，針對 Window x86 目標的 DirectXMath 程式庫進行編譯時，是使用 \_ \_ 已定義的 SSE SSE \_ 內建函式來完成 \_ 。 這表示所有 DirectXMath 功能都會使用 SSE2 指令。 不過，其他程式碼則不是如此。

DirectXMath 之外的程式碼是使用編譯器預設值進行處理。 如果沒有這個參數，所產生的程式碼通常可能會使用較不有效率的 x87 程式碼。

強烈建議您一律使用最新的可用編譯器版本。

## <a name="use-est-functions-when-appropriate"></a>適當時使用 Est 函數

許多函式都有對等的估計函數，以 Est 結尾。 這些函式會以更佳的效能來提高效能。 Est 函式適用于不重要的計算，可能會犧牲精確度以加快速度。 確切的遺失精確度和速度增加的數量取決於平臺。

例如， [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) 函式可用來取代 [**XMVector3AngleBetweenNormals**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) 函數。

## <a name="use-aligned-data-types-and-operations"></a>使用對齊的資料類型和作業

SIMD 指令集在支援 SSE2 的 windows 版本上，通常會有對齊和未對齊的記憶體作業版本。 您可以更快速地使用對齊的作業，而且應該盡可能進行建議。

DirectXMath 程式庫透過 variant 向量類型、結構和函式提供存取對齊和未對齊的功能。 這些變數會以名稱結尾的 "A" 表示。

例如，有一個未對齊的 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) 結構和對齊的 [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) 結構，分別由 [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) 和 [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) 函式使用。

## <a name="properly-align-allocations"></a>適當地對齊配置

DirectXMath 程式庫基礎的 [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) 內建函式的對齊版本，會比未對齊的程式更快。

基於這個理由，使用 [**XMVECTOR**](xmvector-data-type.md) 和 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 物件的 DirectXMath 作業會假設這些物件已對齊16位元組。 這是自動進行堆疊型配置，如果程式碼是使用建議的 Windows 針對 DirectXMath 程式庫進行編譯 (請參閱[使用正確的編譯設定](#use-correct-compilation-settings)) 編譯器設定。 不過，請務必確保包含 **XMVECTOR** 和 **XMMATRIX** 物件的堆積配置，或轉換成這些類型，以符合這些對齊需求。

雖然64位 Windows 記憶體配置已對齊16位元組，但根據預設，在配置的 Windows 記憶體的32位版本中，只會對齊8個位元組。 如需控制記憶體對齊的詳細資訊，請參閱[ \_ 對齊的 \_ malloc](https://docs.microsoft.com/cpp/c-runtime-library/reference/aligned-malloc)。

使用對齊的 DirectXMath 類型搭配標準範本庫 (STL) 時，您必須提供自訂配置器，以確保16位元組的對齊。 如需撰寫自訂配置器的範例，請參閱 Visual C++ Team [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) (而不是使用 malloc/free，您會想要 \_ \_ \_ \_ 在您的實施) 中使用對齊的 malloc 並保持可用。

> [!Note]  
> 某些 STL 範本會修改提供的型別對齊。 例如， [讓 \_ 共用<>](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) 新增一些內部追蹤資訊，而這些資訊不一定會與所提供使用者類型的對齊，而導致資料成員未對齊。 在此情況下，您需要使用未對齊的類型，而不是對齊類型。 如果您衍生自現有的類別（包括許多 Windows 執行階段物件），您也可以修改類別或結構的對齊方式。

 

## <a name="avoid-operator-overloads-when-possible"></a>盡可能避免運算子多載

為了方便起見， [**XMVECTOR**](xmvector-data-type.md) 和 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 之類的一些類型具有一般算數運算的運算子多載。 這類運算子多載通常會建立許多暫存物件。 建議您避免在效能敏感的程式碼中執行這些運算子多載。

## <a name="denormals"></a>非正規數

為了支援接近0的計算，IEEE 754 浮點數標準包含漸進下溢的支援。 逐漸下溢是透過使用反正規化值來實行，而許多硬體實作為處理 denormals 時的速度很慢。 要考慮的優化是針對 DirectXMath 所使用的向量作業停用 denormals 處理。

變更 denormals 的處理是藉由線上程上使用[ \_ controlfp \_ ](/cpp/c-runtime-library/reference/controlfp-s)的常式來完成，而且可能會導致效能改進。 使用此程式碼來變更 denormals 的處理：


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> 在64位版本的 Windows 上，會將[SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))指令用於所有計算，而不只是向量作業。 變更 denormal 處理會影響程式中的所有浮點運算，而不只是 DirectXMath 所使用的向量作業。

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>利用整數浮點數類雙重特性

DirectXMath 支援以四個單精確度浮點數或 4 32 位 (帶正負號或不帶正負號) 值的向量。

由於用來實 DirectXMath 程式庫的指令集會讓您將相同的資料視為多個不同的類型（例如，將相同的向量視為浮點數和整數資料），因此可以達成特定的優化功能。 您可以使用整數向量初始化常式和位運算運算子來取得這些優化，以操作浮點值。

DirectXMath 程式庫所使用之單精確度浮點數的二進位格式，完全符合 IEEE 764 標準：

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

使用 IEEE 764 單一精確度浮點數時，請務必記住，某些標記法具有特殊意義 (也就是說，它們不符合上述描述) 。 範例包括：

-   正零為0
-   負零是0x80000000
-   Q \_ NAN 為07FC0000
-   + INF 0x7F800000
-   -INF 0xFF800000

## <a name="prefer-template-forms"></a>偏好範本表單

[**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle)、 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)、 [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert)、 [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft)、 [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)和 [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright)的範本形式存在。 使用這些取代一般的函式表單，可讓編譯器建立更多提升企業效率的實作為。 對於 [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))，這通常會折迭為一或兩個 \_ mm \_ 隨機的 \_ ps 值。 針對 ARM-霓虹燈， **XMVectorSwizzle** 範本可以利用一些特殊案例，而不是更一般的 VTBL swizzle/置換。

## <a name="using-directxmath-with-direct3d"></a>搭配使用 DirectXMath 與 Direct3D

DirectXMath 的常見用途是執行與 Direct3D 搭配使用的圖形計算。 使用 Direct3D 2.x 和 Direct3D 11. x，您可以透過下列直接方式來使用 DirectXMath 程式庫：

-   在 [**>id3d11devicecoNtext：： ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview)或 [**ID3D10Device：： ClearRenderTargetView**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview)方法的呼叫中，直接在 *ColorRGBA* 參數中使用色彩命名空間 [常數](ovw-xnamath-reference-constants.md)。 針對 Direct3D 9，您必須轉換成 [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)型別，以在 [**IDirect3DDevice9：： Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)方法的呼叫中使用它做為 *Color* 參數。
-   使用 [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md)和 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)型別來設定常數緩衝區結構，以供 HLSL [**float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md)或 [**矩陣**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4 類型參考。
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) /[**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)類型是以資料列為主的格式。 因此，如果您使用/Zpr 編譯器參數 ([**D3DCOMPILE \_ PACK 矩陣資料 \_ 行 \_ \_ 主要**](../direct3dhlsl/d3dcompile-constants.md) 編譯旗標) 或在 \_ HLSL 中宣告矩陣類型時省略 row 主要 [關鍵字](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md) ，則當您將矩陣設定為常數緩衝區時，就必須將它變換。

     

-   使用 Direct3D 2.x 和 Direct3D 11. x，您可以假設 Map 方法所傳回的指標 (例如， **.pdata** 成員 ([**D3D10 \_ 對應 \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d)中的 [**>id3d11devicecoNtext：： map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) 。**.Pdata**、 [**D3D10 \_ 對應的 \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d)。**.Pdata**，或 [**D3D11 \_ 對應的 \_ SUBRESOURCE**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource)。如果您使用 [功能層級](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)10 \_ 0 或更高版本，或每次使用 [**D3D11 \_ 使用量 \_ 暫存**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)資源，.pdata) 會對齊16位元組。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式設計指南](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
