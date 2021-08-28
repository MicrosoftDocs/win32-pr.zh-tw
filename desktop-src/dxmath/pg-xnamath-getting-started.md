---
title: '開始 (DirectXMath) '
description: DirectXMath 程式庫會針對單精確度浮點數向量（ (2D、3D 和 4D) 或矩陣 (3 ×3和4× 4) ），來實作為算術和線性代數運算的最佳和可移植介面。
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ad7de99a462dc533d8010c45dfadcb1bcfa1b6f33317a941e91c16f30c3d2c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117498"
---
# <a name="getting-started-directxmath"></a>開始 (DirectXMath) 

DirectXMath 程式庫會針對單精確度浮點數向量（ (2D、3D 和 4D) 或矩陣 (3 ×3和4× 4) ），來實作為算術和線性代數運算的最佳和可移植介面。 程式庫對整數向量作業的支援有限。 圖形程式會廣泛地使用這些作業來呈現和動畫。 不支援雙精確度向量 (包括長、短路或 bytes) ，以及只有有限的整數向量運算。

此程式庫可在各種不同的 Windows 平臺上使用。 因為此程式庫提供了先前無法使用的功能，所以這個版本會取代下列程式庫：

-   Xboxmath .h 標頭所提供的 Xbox 數學程式庫
-   D3DX 9 Dll 提供的 D3DX 9 程式庫
-   透過 D3DX 10 Dll 提供的 D3DX 10 數學程式庫
-   DirectX SDK 和 Xbox 360 XDK 中的 xnamath. h 標頭所提供的不帶數學程式庫

這些章節概述開始使用的基本概念。

-   [下載](#download)
-   [執行時間系統需求](#run-time-system-requirements)
-   [設計總覽](#design-overview)
-   [矩陣慣例](#matrix-convention)
-   [基本使用方式](#basic-usage)
-   [類型使用指導方針](#type-usage-guidelines)
-   [建立向量](#creating-vectors)
    -   [常數向量](#constant-vectors)
    -   [變數中的向量](#vectors-from-variables)
    -   [向量的向量](#vectors-from-vectors)
    -   [記憶體中的向量](#vectors-from-memory)
-   [從向量解壓縮元件](#extracting-components-from-vectors)
-   [相關主題](#related-topics)

## <a name="download"></a>下載

DirectXMath 程式庫包含在 Windows SDK 中。 或者，您也可以從[GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath)下載它。 此網站也包含相關的範例專案。

## <a name="run-time-system-requirements"></a>Run-Time 系統需求

DirectXMath 程式庫會在向量作業可用時，使用特製化的處理器指令。 若要避免程式產生「未知的指令例外狀況」錯誤，請先呼叫 [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) ，然後再使用 DirectXMath 程式庫來檢查處理器支援。

以下是基本的 DirectXMath 程式庫執行時間支援需求：

-   Windows (x86/x64) 平臺上的預設編譯需要 SSE/SSE2 指令支援。
-   Windows RT 平臺上的預設編譯需要 ARM-霓虹燈指令支援。
-   使用 XM 進行編譯時， [**\_ \_ 未定義任何 \_ 內建函式 \_**](ovw-xnamath-reference-directives.md) ，只需要標準的浮點運算支援。

> [!Note]  
> 當您呼叫 [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport)時，請包含 <的>，然後再包含 <DirectXMath. h>。 這是程式庫中唯一需要 <windows. h> 中之內容的函式，因此您不需要在使用 <DirectXMath 的每個模組中包含 <的 windows. h>。

 

## <a name="design-overview"></a>設計概觀

DirectXMath 程式庫主要支援 c + + 程式設計語言。 此程式庫是使用 DirectXMath \* . .inl、DirectXPackedVector. .inl 和 DirectXCollision. .inl 中的內嵌常式來執行。 這項實行會使用高效能編譯器內建函式。

DirectXMath 程式庫提供：

-   使用 SSE/SSE2 內建函式的實作為。
-   沒有內建函式的執行。
-   使用 ARM 霓虹燈內建函式的實作為。

因為程式庫是使用標頭檔來傳遞，所以請使用原始程式碼針對您自己的應用程式自訂和優化。

## <a name="matrix-convention"></a>矩陣慣例

DirectXMath 使用資料列主要矩陣、資料列向量和預先相乘。 Handedness 取決於 (RH 與 LH) 所使用的函式版本，否則函數會使用左手或右手的視圖座標。

為了進行參考，Direct3D 先前使用了左方座標系統、資料列主要矩陣、資料列向量和預先相乘。 新式 Direct3D 並不具有左方和右手方座標的強大需求，而且通常會 HLSL 著色器預設為使用資料行主要矩陣。 如需詳細資料，請參閱 [HLSL 矩陣順序](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) 。

## <a name="basic-usage"></a>基本使用方式

若要使用 DirectXMath 程式庫函式，請包含 DirectXMath .h、DirectXPackedVector .h、DirectXColors .h 及/或 DirectXCollision .h 標頭。 這些標頭可在 Windows Store 應用程式的 Windows 軟體開發套件中找到。

## <a name="type-usage-guidelines"></a>類型使用指導方針

[**XMVECTOR**](xmvector-data-type.md)和 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)類型是 DirectXMath 程式庫的工作馬。 每個作業都會耗用或產生這些類型的資料。 使用程式庫是使用程式庫的關鍵。 不過，由於 DirectXMath 會使用 SIMD 指令集，因此這些資料類型會受到一些限制。 如果您想要充分利用 DirectXMath 函式，請務必瞭解這些限制。

您應該將 [**XMVECTOR**](xmvector-data-type.md) 視為 SIMD 硬體登錄的 proxy，以及 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 為四個 simd 硬體暫存器邏輯群組的 proxy。 這些類型會標注，表示它們需要16位元組對齊才能正確運作。 編譯器會在做為區域變數時，自動將它們放置在堆疊上，或在當做全域變數使用時，將它們放在資料區段中。 有了適當的慣例，也可以安全地將它們當作參數傳遞給函式 (如需詳細資訊) ，請參閱 [呼叫慣例](pg-xnamath-internals.md) 。

不過，堆積的配置更為複雜。 因此，每當您使用 [**XMVECTOR**](xmvector-data-type.md) 或 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 做為類別或結構的成員，以從堆積配置時，您就必須特別小心。 在 Windows x64 上，所有堆積配置都已對齊16位元組，但針對 Windows x86，則只會對齊8個位元組。 有一些選項可從堆積配置16位元組對齊的結構 (請參閱 [適當地對齊](pg-xnamath-optimizing.md) 配置) 。 針對 c + + 程式，您可以使用 operator new/delete/new/delete 多載 \[ \] \[ \] (全域或特定類別) ，視需要強制執行最佳對齊。

> [!Note]  
> 替代方法是在 c + + 類別中直接藉由多載新的/刪除來強制對齊，您可以使用 [pImpl 的用法](https://en.wikipedia.org/wiki/Opaque_pointer)。 如果您確定您的 **Impl** 類別透過內部 [**\_ 對齊的 \_ malloc**](/cpp/c-runtime-library/reference/aligned-malloc)對齊，您就可以在內部執行中自由使用對齊的類型。 當 ' public ' 類別是 Windows 執行階段 ref 類別，或要與 [**std：： shared \_ ptr<>**](/cpp/standard-library/shared-ptr-class)搭配使用時，這會是很好的選項，否則可能會中斷密切對齊。

 

不過，通常更容易且更精簡，以避免直接在類別或結構中使用 [**XMVECTOR**](xmvector-data-type.md) 或 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 。 相反地，請使用 [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)、 [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)、 [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3)、 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)等作為結構的成員。 此外，您可以使用 [向量載入](ovw-xnamath-reference-functions-load.md)和 [向量儲存體](ovw-xnamath-reference-functions-storage.md)函式，將資料有效率地移至 **XMVECTOR** 或 **XMMATRIX** 區域變數，執行計算並儲存結果。 另外還有串流處理函式 ([**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)、 [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)等，在這些資料類型的陣列上有效率地直接操作的) 。

## <a name="creating-vectors"></a>建立向量

### <a name="constant-vectors"></a>常數向量

許多作業都需要在向量計算中使用常數，而且有數種方式可以載入具有所需值的 [**XMVECTOR**](xmvector-data-type.md) 。

-   如果將純量常數載入至 [**XMVECTOR**](xmvector-data-type.md)的所有元素，請使用 [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) 或 [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)。
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   如果使用具有不同固定值的向量常數作為 [**XMVECTOR**](xmvector-data-type.md)，請使用 [**XMVECTORF32**](xmvectorf32-data-type.md)、 [**XMVECTORU32**](xmvectoru32-data-type.md)、 **XMVECTORI32** 或 [**XMVECTORU8**](xmvectoru8-data-type.md) 結構。 然後您可以直接參考您傳遞 **XMVECTOR** 值的任何位置。
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > 請勿直接使用具有 [**XMVECTOR**](xmvector-data-type.md) (的初始化運算式清單，也就是 XMVECTOR v = {1.0 f，2.0 f，3.0 f，4.0 f} ) 。 這類程式碼的效率不佳，而且在 DirectXMath 支援的所有平臺上都無法移植。

     

-   DirectXMath 包含數個預先定義的全域常數，可讓您在程式碼中使用 (g \_ XMOne、g \_ XMOne3、g \_ XMTwo、g \_ XMOneHalf、g \_ XMHalfPi、g \_ XMPi 等) 。 在 DirectXMath. h 標頭中搜尋 **XMGLOBALCONSTANT** 值。
-   常見 RGB 色彩有一組向量常數 (紅色、綠色、藍色、黃色等) 。 如需這些向量常數的詳細資訊，請參閱 DirectXColors .h 和 DirectX：： Colors 命名空間。

### <a name="vectors-from-variables"></a>變數中的向量

-   如果從單一純量變數建立向量，請參閱 [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) 和 [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)。
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   如果從四個純量變數建立向量，請參閱 [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) 和 [**XMVectorSetInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint)。
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a>向量的向量

-   如果從另一個向量建立向量，並將特定的元件設定為變數，您可以考慮使用 [向量存取子函數](ovw-xnamath-reference-functions-accessors.md)。
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   如果從另一個已複寫單一元件的向量建立向量，請使用 [**XMVectorSplatX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx)、 [**XMVectorSplatY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty)、 [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)和 [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw)。
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   如果從另一個向量或不同向量（具有重新排序的元件）建立向量，請參閱 [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) 和 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)。
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a>記憶體中的向量

-   若要從記憶體載入單一 float 值，請參閱 [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr)、 [**XMVectorReplicateIntPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr)、 [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)和 [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint)。
-   載入 float 陣列的常見方式是： [**XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2)、 [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3)、 [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4)、 [**XMLoadFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3)、 [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)和 [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4)。
-   DirectXMath 包含一組豐富的型別和相關的負載，以及用來處理各種資料結構和常見 GPU 格式的存放區。 請參閱 [向量載入](ovw-xnamath-reference-functions-load.md) 和 [向量存放區](ovw-xnamath-reference-functions-storage.md)。

## <a name="extracting-components-from-vectors"></a>從向量解壓縮元件

當資料載入 SIMD 暫存器，並在解壓縮結果之前完整處理時，SIMD 處理最有效率。 純量和向量表單之間的轉換效率不佳，因此我們建議您只在必要時才這樣做。 基於這個理由，DirectXMath 程式庫中產生純量值的函式會以向量形式傳回，其中純量結果會在產生的向量之間複寫， (也就是， [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot)、 [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)等) 。 但是，當您需要純量值時，以下是一些如何做的選擇：

-   如果計算單一純量答案，則適用 [向量存取](ovw-xnamath-reference-functions-accessors.md) 子函式的用法如下：
    ```
    float f = XMVectorGetX( v );
    ```

    

-   如果需要將向量的多個元件解壓縮，請考慮將向量儲存在記憶體結構中，然後將它讀回。 例如：
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   向量處理最有效率的形式是使用記憶體對記憶體串流，其中會使用 [向量載入](ovw-xnamath-reference-functions-load.md) 函式從記憶體載入輸入資料 () 、完整地以 SIMD 形式處理，然後寫入記憶體 () 使用 [向量存放函數](ovw-xnamath-reference-functions-storage.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式設計指南](ovw-xnamath-progguide.md)
</dt> </dl>

 

 