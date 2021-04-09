---
description: 此資料表會將 FVF 碼對應至 D3DVERTEXELEMENT9 結構。
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: '將 FVF 碼對應至 direct3d 9 宣告 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85442cf1c92c78aa1a37f4d4a4ec3de154f5b8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687360"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>將 FVF 碼對應至 direct3d 9 宣告 (Direct3D 9) 

此資料表會將 FVF 碼對應至 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 結構。



| FVF                                                   | 資料類型                                                           | 使用方式                                                                         | 使用方式索引 |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ XYZ                                           | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ 位置                                                        | 0           |
| D3DFVF \_ XYZRHW                                        | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ POSITIONT                                                       | 0           |
| D3DFVF \_ XYZW                                          | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ 位置                                                        | 0           |
| D3DFVF \_ XYZB5 與 D3DFVF \_ LASTBETA \_ UBYTE4            | D3DVSDT \_ FLOAT3、D3DVSDT \_ FLOAT4、D3DVSDT \_ UBYTE4                   | D3DDECLUSAGE \_ POSITION、D3DDECLUSAGE \_ BLENDWEIGHT、D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5 與 D3DFVF \_ LASTBETA \_ D3DCOLOR          | D3DVSDT \_ FLOAT3、D3DVSDT \_ FLOAT4、D3DVSDT \_ D3DCOLOR                 | D3DDECLUSAGE \_ POSITION、D3DDECLUSAGE \_ BLENDWEIGHT、D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5                                         | D3DDECLTYPE \_ FLOAT3、D3DDECLTYPE \_ FLOAT4、D3DDECLTYPE \_ FLOAT1       | D3DDECLUSAGE \_ POSITION、D3DDECLUSAGE \_ BLENDWEIGHT、D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n = 1 ... 4)                                 | D3DDECLTYPE \_ FLOAT3、D3DDECLTYPE \_ FLOATn                            | D3DDECLUSAGE \_ 位置，D3DDECLUSAGE \_ BLENDWEIGHT                             | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4) 和 D3DFVF \_ LASTBETA \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3、D3DDECLTYPE \_ FLOAT (n-1) 、D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ POSITION、D3DDECLUSAGE \_ BLENDWEIGHT、D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4) 和 D3DFVF \_ LASTBETA \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3、D3DDECLTYPE \_ FLOAT (n-1) 、D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ POSITION、D3DDECLUSAGE \_ BLENDWEIGHT、D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ 正常                                        | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ 正常                                                          | 0           |
| D3DFVF \_ PSIZE                                         | D3DDECLTYPE \_ FLOAT1                                                 | D3DDECLUSAGE \_ PSIZE                                                           | 0           |
| D3DFVF \_ 擴散                                       | D3DDECLTYPE \_ D3DCOLOR                                               | D3DDECLUSAGE \_ 色彩                                                           | 0           |
| D3DFVF \_ 反光                                      | D3DDECLTYPE \_ D3DCOLOR                                               | D3DDECLUSAGE \_ 色彩                                                           | 1           |
| D3DFVF \_ TEXCOORDSIZEm (n)                               | D3DDECLTYPE \_ FLOATm                                                 | D3DDECLUSAGE \_ TEXCOORD                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>使用 D3DDECLUSAGE POSITIONT 的頂點宣告 \_

使用 (D3DUSAGE POSITIONT，0) 的頂點元素是否存在 \_ ，是用來向裝置指出即將進行的頂點資料已通過頂點處理 (例如 FVF D3DFVF \_ XYZRHW 位設定) 。 在繪製時期，如果目前設定的宣告具有 (D3DUSAGE POSITIONT 的元素 \_ ，0) 語義，則會略過整個頂點處理， (就像已 \_) 設定 D3DFVF XYZRHW 位的 FVF 一樣。

使用 (D3DDECLUSAGE \_ POSITIONT，0) 的頂點宣告有一些限制：

-   只有資料流程零可以用在這類宣告中。
-   頂點元素必須藉由增加資料流程位移來排序。
-   資料流程位移必須對齊 DWORD。
-   相同的 (使用量，使用方式索引) 組應該只會列出一次。
-   只能使用 D3DDECLMETHOD 的 \_ 預設方法。
-   其他頂點元素不能有 (D3DDECLUSAGE \_ 位置，0) 語義。

此外，與設備磁碟機版本相關的這類宣告也有一些限制。 這些限制是有效的，因為 Direct3D 會直接將這類宣告傳送到驅動程式，而不會進行任何轉換。

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>沒有 D3DDECLUSAGE POSITIONT 的頂點宣告 \_

執行時間會驗證宣告的建立。 以下是合法宣告的一般規則。

-   資料流程的所有頂點元素都必須是連續的，並且依位移排序。
-   資料流程位移必須對齊 DWORD。
-   相同的 (使用量，使用方式索引) 組應該只會列出一次。
-   如果 \_ 已設定 D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET，
    -   多個頂點元素可以在資料流程中共用相同的位移。
    -   頂點元素可以是不同的類型，而這些類型可以不同的大小。
    -   頂點元素可以任意重迭。 例如，一個元素可以從資料流程的位置開始，也就是在另一個專案的中間。
    -   頂點元素允許以任何順序有資料流程位移。
-   頂點元素的數目不可大於64。
-   UsageIndex 應該在0-15 範圍內 \[ \] 。
-   宣告（搭配 DrawPrimitive API 使用）不應該有 D3DDECLMETHOD \_ DEFAULT、D3DDECLMETHOD \_ LOOKUPPRESAMPLED 或 D3DDECLMETHOD LOOKUP 以外的頂點元素 \_ 。
-   宣告（包含 D3DDECLMETHOD \_ LOOKUP 或 LOOKUPPRESAMPLED）只能搭配可程式化的頂點管線使用。
-   搭配 DrawRectPatch/DrawTriPatch API 使用的宣告不能有具有 D3DDECLMETHOD \_ LOOKUPPRESAMPLED 或 D3DDECLMETHOD LOOKUP 的頂點元素 \_ 。
-   宣告只能有一個具有 D3DDECLMETHOD \_ LOOKUP 或 D3DDECLMETHOD \_ LOOKUPPRESAMPLED 方法的元素。
-   具有 D3DDECLMETHOD \_ LOOKUP 或 D3DDECLMETHOD LOOKUPPRESAMPLED 的宣告 \_ 不能有 D3DDECLMETHOD 預設值以外的專案 \_ ，因為只有 N 個修補程式才會執行置換對應。
-   具有 D3DDECLMETHOD \_ LOOKUP 或 D3DDECLMETHOD LOOKUPPRESAMPLED 的頂點元素 \_ 只能與 (D3DDECLUSAGE 範例搭配使用 \_ ，n) 語義，反之亦然。
-   如果具有 D3DDECLMETHOD LOOKUP 方法的頂點元素 \_ 有資料流程索引和已存在頂點專案的位移，則這個頂點元素應該具有相同的資料類型。
-   具有 D3DDECLMETHOD LOOKUP 方法的頂點元素 \_ 應該具有 D3DDECLTYPE \_ FLOAT2/3/4 資料類型
-   類型為 D3DDECLMETHOD \_ CROSSUV、D3DDECLMETHOD \_ PARTIALU 和 D3DDECLMETHOD PARTIALV 的頂點元素 \_ 應具有具有相容資料類型的頂點元素位移。
-   具有方法 D3DDECLMETHOD \_ UV 或 D3DDECLMETHOD LOOKUPPRESAMPLED 的頂點元素 \_ ，必須有類型 D3DDECLTYPE \_ 未使用、資料流程索引零和資料流程位移零。
-   具有方法的宣告 D3DDECLMETHOD \_ UV、D3DDECLMETHOD \_ PARTIALU 和 D3DDECLMETHOD \_ PARTIALV 只能搭配 DrawRectPatch 使用。
-   Usage D3DDECLUSAGE \_ TESSFACTOR 只能搭配 D3DDECLTYPE \_ FLOAT1 和 usage index 0 資料類型使用。
-   當宣告用於鑲嵌式 (DrawRectPatch、DrawTriPatch、N 修補程式) 時，資料類型必須小於或等於 D3DDECLTYPE \_ SHORT4。
-   包含需要特定裝置功能之方法的宣告 (例如，置換對應、RT 修補程式) 只有在裝置支援時才能建立。
-   用來繪製點和線條的頂點宣告不能有 D3DDECLMETHOD 預設值以外的方法 \_ 。
-   可以建立的宣告也取決於驅動程式功能。

## <a name="driver-considerations"></a>驅動程式考慮

### <a name="pre-direct3d-9-drivers"></a>預先 Direct3D 9 驅動程式

-   輸入宣告必須可翻譯成有效的 FVF (具有相同的頂點元素順序和其資料類型) 。
-   不允許材質座標中的間隙。 這表示，如果有一個頂點元素有 (D3DDECLUSAGE \_ TEXCOORD、n) 然後也應該有一個頂點元素 (D3DDECLUSAGE \_ TEXCOORD，n-1) 。

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>不含圖元著色器第3版支援的 Direct3D 9 驅動程式

-   輸入宣告必須可翻譯成有效的 FVF (具有相同的頂點元素順序和其資料類型) 。
-   允許材質座標中的間隙。

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>具有圖元著色器第3版支援的 Direct3D 9 驅動程式

允許更多一般宣告。

-   頂點元素可以任意順序，而且可以有任何資料類型。
-   如果裝置已設定 D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET，則多個頂點元素可以共用相同的資料流程位移和不同的類型 \_ 。

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>使用可程式化頂點管線的頂點宣告用法

-   在繪圖時，Direct3D 會在目前的頂點宣告和目前的頂點著色器函式中尋找相同的「使用量-使用方式索引」組合。 找到組合時，會使用來自著色器函式的暫存器做為頂點元素的目的地。
-   當目前頂點宣告中的頂點元素有在目前頂點著色器中找不到的使用方式時，就會忽略該頂點元素。
-   使用小於2.0 的頂點著色器版本時，著色器程式碼中所提及的所有語義都必須存在於繪製時間系結的宣告中。 使用頂點著色器2.0 和更新版本時，允許應用程式使用具有相同頂點著色器之不同頂點宣告的這種限制並不存在。 當頂點著色器根據靜態條件讀取輸入資料時，這非常有用。 端點著色器暫存器未初始化，因為這樣會有未定義的值。

搭配 DirectX 8 驅動程式上的硬體頂點處理使用時，還有其他限制：

-   頂點元素不能重迭或共用相同的位移。
-   資料類型受限於 DirectX 8 驅動程式可瞭解的內容。

如果提供的宣告無法轉換成 DirectX 8 樣式的宣告，CreateVertexDeclaration 可能會失敗。 若為混合模式裝置，則會在繪製時發生此失敗， \* 因為這是您唯一知道此著色器是否與硬體或軟體頂點處理搭配使用的時間。

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>使用 Fixed 函數管線的頂點宣告用法

只能使用符合下列規則的宣告：

-   在用於固定函式管線) 的 DirectX 8 宣告中，不允許在頂點元素之間有間距 (略過。
-   語義 (D3DDECLUSAGE \_ 位置，必須指定 0) ，而且應該具有 D3DDECLTYPE \_ FLOAT3 資料類型。
-   具有方法 D3DDECLMETHOD UV 的頂點元素 \_ 必須指定 USAGE D3DDECLUSAGE \_ TEXCOORD 或 D3DDECLUSAGE \_ BLENDWEIGHT。
-   具有方法 D3DDECLMETHOD \_ PARTIALU、PARTIALV 或 CROSSUV 的頂點元素只能 \_ \_ 與 D3DDECLUSAGE \_ 位置、 \_ 標準、 \_ BLENDWEIGHT 或 TEXCOORD 搭配使用， \_ 而且必須使用輸入類型 D3DDECLTYPE \_ FLOAT3。

當宣告搭配 DirectX 8 驅動程式上的硬體頂點處理使用時，Direct3D 執行時間會將它轉換成 DirectX 8 樣式的宣告，並具有下列規則：

-   頂點元素不能共用資料流程中的相同位移，而且它們不能重迭。
-   資料類型必須小於或等於 D3DDECLTYPE \_ SHORT4。
-   只允許下列方法： D3DDECLMETHOD \_ 預設、D3DDECLMETHOD \_ CROSSUV 和 D3DDECLMETHOD \_ UV
-   [Direct3d 9 宣告與 direct3d 8 宣告之間的對應 (direct3d 9) ](mapping-between-a-directx-9-declaration-and-directx-8.md) 顯示哪些 direct3d 9 語義可以轉換成 DirectX 8 樣式的宣告。 使用方式和 UsageIndex 會轉換成暫存器值。
-   如果宣告中有 n 個頂點元素，而且 0-m (m < n) 對應至 [direct3d 宣告與 FVF 程式碼 (direct3d 9) ) 之間對應 ](mapping-between-a-directx-9-declaration-and-fvf-codes.md) 中所述的 FVF (元素，但 m + 1 則否：
    -   如果有任何 m + 2 到 n 個頂點元素對應至 FVF/dx8decl，則宣告無效。
    -    (DirectX 8 和舊版驅動程式的執行時間會將元素0到 m 轉換，而 Direct3D 9 驅動程式) 使用 Direct3D 宣告 [與 FVF 碼之間的對應 (direct3d 9) ](mapping-between-a-directx-9-declaration-and-fvf-codes.md)，m + 1，m + 2 直到 n-1 對應到連續的 texcoord (k) ，texcoord (k + 1) ，從專案 0-m 的任何 texcoord 開始。
    -   在對應的 texcoord 中，資料類型會假設為 float \[ 1234， \] 取代目前元素包含 (但大小) 相同的任何資料類型。 因此，現有的資料類型可能是在 direct3d 宣告 [和 FVF 程式碼 (direct3d 9) 之間沒有對應 ](mapping-between-a-directx-9-declaration-and-fvf-codes.md)的內容。
    -   如果 k 達到8，FVF/dx8decl 的宣告就會無效。
    -   如果發生 texcoords 的任何對應，則整個宣告都必須沒有任何專案具有非預設的產生方法，否則宣告對 FVF/dx8decl 而言是不正確。

## <a name="using-vertex-declarations-with-processvertices"></a>使用 ProcessVertices 的頂點宣告

頂點宣告可用來描述 ProcessVertices 的輸出。 這類宣告應遵守下列規則：

-   只有資料流程0必須使用。
-   只 \_ 允許 D3DDECLMETHOD 的預設方法。
-   只能 \_ 使用 D3DDECLTYPE FLOATn 或 D3DDECLTYPE \_ D3DCOLOR 資料類型。
-   頂點元素不能共用相同的位移或互相重迭。
-   具有 (D3DDECLUSAGE \_ 位置、0) 或 (D3DDECLUSAGE \_ POSITIONT，0) 的頂點元素不是必要專案。
-   具有 (D3DDECLUSAGE \_ 位置、0) 和 (D3DDECLUSAGE \_ POSITIONT，0) 的頂點元素不能出現在相同的宣告中。
-   使用這類宣告時，目前的頂點著色器必須為3.0 或更高版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點宣告](vertex-declaration.md)
</dt> </dl>

 

 



