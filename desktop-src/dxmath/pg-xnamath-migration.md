---
description: 本總覽說明使用 [DirectXMath] 程式庫將現有程式碼遷移至程式庫所需的變更。
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: 從「設備」數學程式庫進行程式碼遷移
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512688"
---
# <a name="code-migration-from-the-xna-math-library"></a>從「設備」數學程式庫進行程式碼遷移

本總覽說明使用 [DirectXMath] 程式庫將現有程式碼遷移至程式庫所需的變更。

-   [標頭變更](#header-changes)
-   [常數變更](#constant-changes)
-   [命名空間](#namespaces)
-   [部分載入](#partial-loads)
-   [移除 Xbox 360 的特定類型](#removal-of-xbox-360-specific-types)
-   [ARM-霓虹燈內建函式](#arm-neon-intrinsics)
-   [置換](#permute)
-   [範本表單](#template-forms)
-   [消除函式](#eliminated-functions)
-   [相關主題](#related-topics)

## <a name="header-changes"></a>標頭變更

DirectXMath 程式庫會使用一組新的標頭。

以 DirectXMath 取代 xnamath .h 標頭，並為「GPU 已封裝」類型新增 DirectXPackedVector。

Xnacollision 中 DirectX SDK 碰撞範例中的周框類型現在是 DirectXCollision 中 DirectXMath 程式庫的一部分。 這些已修改為使用 c + + 類別，而不是 C 樣式的 API。

## <a name="constant-changes"></a>常數變更

XNAMATH \_ 版本 (200、201、202、203、204等) 已取代為 DIRECXTMATH \_ 版本 (300、301、302、303等) 。

> [!Note]  
> DirectXMath 3.00 和3.02 隨附 Windows SDK 的初步版本。 DirectXMath 3.03 是 Windows 8 SDK 的最終版本。

 

## <a name="namespaces"></a>命名空間

DirectXMath 程式庫會使用 c + + 命名空間來組織類型。 只有全域命名空間才會使用未使用的運算。 DirectXMath 型別在具有「DirectX」或「DirectX：:P ackedVector」命名空間中的常見情況。

在 c + + 原始程式檔中，簡單的解決方案是加入 ' using ' 語句：


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



若為標頭，則不會將它視為「最佳做法」來加入 using 語句。 請改為新增完整命名空間：


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a>部分載入

針對載入小於4個 XMVECTOR 專案的各種函式，未定義的「未定義」專案會保留未定義的其他元素。 DirectXMath 一律會以0填滿這些額外的元素。

## <a name="removal-of-xbox-360-specific-types"></a>移除 Xbox 360 的特定類型

DirectXMath 中無法使用下列未使用的數學程式庫類型、函數和常數。

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3 () 、XMLoadHenD3 () 、XMLoadUHenDN3 () 、XMLoadUHenD3 () 、XMLoadDHenN3 () 、XMLoadDHen3 () 、XMLoadUDHenN3 () 、XMLoadUDHen3 () 
-   XMStoreHenDN3 () 、XMStoreHenD3 () 、XMStoreUHenDN3 () 、XMStoreUHenD3 () 、XMStoreDHenN3 () 、XMStoreDHen3 () 、XMStoreUDHenN3 () 、XMStoreUDHen3 () 
-   g \_ XMMaskHenD3、g \_ XMMaskDHen3、g \_ XMAddUHenD3、g \_ XMAddHenD3、g \_ XMAddDHen、g \_ XMMulHenD3、g \_ XMMulDHen3、g \_ XMXorHenD3、g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4 () 、XMLoadXIco4 () 、XMLoadIcoN4 () 、XMLoadIco4 () 、XMLoadUIcoN4 () 、XMLoadUIco4 () 
-   XMStoreXIcoN4 () 、XMStoreXIco4 () 、XMStoreIcoN4 () 、XMStoreIco4 () 、XMStoreUIcoN4 () 、XMStoreUIco4 () 
-   g \_ XMMaskIco4、g \_ XMXorXIco4、g \_ XMXorIco4、g \_ XMAddXIco4、g \_ XMAddUIco4、g \_ XMAddIco4、g \_ XMMulIco4

\_\_vector4i 已被取代。 請改用 [**XMVECTORI32**](xmvectori32-data-type.md) 或 [**XMVECTORU32**](xmvectoru32-data-type.md) 。

下列函數和類型已被取代，因為它們只 Xbox 360： XMLoadDecN4、XMStoreDecN4、XMDECN4、XMLoadDec4、XMStoreDec4、XMDEC4、XMLoadXDec4、XMStoreXDec4、XMXDEC4。

## <a name="arm-neon-intrinsics"></a>ARM-霓虹燈內建函式

使用此程式碼宣告向量常數，將會針對 SSE 和無內建的未處理數學進行編譯，但使用 ARM 的 DirectXMath 將會失敗。


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



一般而言，我們不建議使用這種方法來初始化 [**XMVECTOR**](xmvector-data-type.md)。 但是，如果您想要向量常數， [**XMVECTORF32**](xmvectorf32-data-type.md) 類別支援這種初始化樣式，並會自動傳回 **XMVECTOR** 型別，因此您可以在大部分的相同內容中使用 **XMVECTORF32** 。 **XMVECTORF32** 類別的任何寫入作業都需要明確參考. v **XMVECTOR** 成員。

## <a name="permute"></a>置換

在一般向量置換中，「執行程式數學程式庫」具有下列形式：


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



若為 DirectXMath， **XMVectorPermuteControl** 已被刪除，而 XM \_ 置換 \_ 0x。 \_置換 \_ 1Z 常數已重新定義為簡單的0-7 索引。 以下是 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)的新簽章：


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



這個函式不會使用控制字組，而是直接採用4個索引做為參數，也就是使用新的 XM SWIZZLE X 來使其類似于 [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) 函式 \_ \_ 。 \_SWIZZLE \_ ，W 常數定義為簡單的0-3 索引。


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> 針對常數值，有更有效率的方式來執行置換。 使用 **範本** 表單，而不是使用 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)的函式形式：
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a>範本表單
>
> 一般情況下，使用範本形式的函式形式的下列函式會更有效率，而且可讓程式庫透過範本特製化來執行平臺特定的優化。
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a>消除函式
>
> 
>
> | 刪除函式        | 取代                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) 嗎？ [XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0 |
> | XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) 嗎？ [XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0 |
> | XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) 嗎？ [XM \_CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) ：0 |
> | XMVectorCosHEst            | [**XMVectorCosH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | XMVectorExpEst             | [**XMVectorExp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | XMVectorLogEst             | [**XMVectorLog**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | XMVectorPowEst             | [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | XMVectorSinHEst            | [**XMVectorSinH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | XMVectorTanHEst            | [**XMVectorTanH**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a>相關主題
>
> <dl> <dt>

[DirectXMath 程式設計指南](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
