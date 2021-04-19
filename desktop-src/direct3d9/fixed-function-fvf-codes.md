---
description: FVF 程式碼會描述在單一資料流程中，以交錯方式儲存的頂點內容。
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: 修正 (Direct3D 9) 的函式 FVF 碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970274"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>修正 (Direct3D 9) 的函式 FVF 碼

FVF 程式碼會描述在單一資料流程中，以交錯方式儲存的頂點內容。 它通常會指定固定函式頂點處理管線所要處理的資料。 這是較舊樣式的頂點宣告;若要查看目前的頂點宣告樣式，請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。

Direct3D 應用程式可以透過數種不同的方式來定義模型頂點。 支援彈性頂點定義（也稱為彈性頂點格式或彈性頂點格式的程式碼），讓您的應用程式可以只使用它所需的頂點元件，以排除未使用的元件。 藉由只使用所需的頂點元件，您的應用程式可以節省記憶體，並將呈現模型所需的處理頻寬降至最低。 您可以使用 [D3DFVF](d3dfvf.md) 碼的組合來描述頂點的格式化方式。

FVF 規格包含 D3DFVF PSIZE 所指定的點大小格式 \_ 。 這種大小是以相機空間單位表示，適用于非轉換和亮 (TL) 頂點，以及在 TL 頂點的裝置空間單位中。

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的轉譯方法會使用接受這些旗標組合的方法來提供 c + + 應用程式，並使用它們來決定如何呈現基本專案。 基本上，這些旗標會告訴系統哪些頂點元件-位置、頂點混色加權、正常、色彩，以及紋理座標的數目和格式-您的應用程式會使用和間接地使用您希望 Direct3D 套用至哪些轉譯管線部分。 此外，特定頂點格式旗標的存在與否會與系統通訊，也就是有哪些頂點元件欄位存在於記憶體中，以及您省略了哪些。

若要判斷裝置的限制，您可以 \_ \_ 在 [**FVFCaps**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 D3DCAPS9 成員中，查詢裝置的 D3DFVFCAPS DONOTSTRIPELEMENTS 和 D3DFVFCAPS TEXCOORDCOUNTMASK 的值。

您可以使用不同的格式來宣告材質座標，讓材質可以使用最少的一個座標，或多達四個材質座標來定址， (2D 投射的材質座標) 。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質座標格式 ](texture-coordinate-formats.md)。 使用 [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) 的宏集來建立位模式，以識別頂點格式所使用的材質座標格式。

沒有任何應用程式會使用每個元件。 互異的同質 W (RHW) 和頂點一般欄位互斥。 大部分的應用程式也都不會嘗試使用所有八組紋理座標，但是 Direct3D 具有這個容量。 您可以搭配其他旗標使用的旗標有幾項限制。 例如，您不能同時使用 D3DFVF \_ XYZ 和 D3DFVF \_ XYZRHW 旗標，因為這表示您的應用程式會使用未轉換和已轉換的頂點來描述頂點的位置。

若要使用索引頂點混色，D3DFVF \_ LASTBETA \_ UBYTE4 旗標應該會出現在 FVF 宣告的結尾。 此旗標的存在表示第五個混色加權將被視為 DWORD 而不是 float。 如需詳細資訊，請參閱 [ (Direct3D 9) 的索引頂點混色 ](indexed-vertex-blending.md)。

下列程式碼範例顯示使用 D3DFVF LASTBETA UBYTE4 旗標的 FVF 程式碼與不是的程式碼之間的差異 \_ \_ 。 \_使用四個混合索引時，會出現旗標 D3DFVF XYZB3，因為您一律會從數位1減去前三個的總和，以取得第四個 (blend ₄ = 1- (blend ₁ + blend ₂ + blend ₃) ) 。


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



以下定義的 FVF 會使用 D3DFVF \_ LAST \_ UBYTE4 旗標。


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點宣告](vertex-declaration.md)
</dt> </dl>

 

 
