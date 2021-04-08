---
description: " (Direct3D 9) 的鑲嵌"
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: " (Direct3D 9) 的鑲嵌"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688144"
---
# <a name="tessellation-direct3d-9"></a> (Direct3D 9) 的鑲嵌

## <a name="tessellator-unit"></a>鑲嵌單位

已增強鑲嵌單位。 您現在可以使用它來：

-   執行所有高序位基本專案的調適型鑲嵌。
-   從置換地圖中查詢每個頂點的位移值，並將其傳遞至頂點著色器。
-   支援矩形-修補程式鑲嵌。 這是透過使用 D3DDECLMETHOD \_ PARTIALU 或 D3DDECLMETHOD PARTIALV 的頂點宣告來指定 \_ 。 如果使用包含這些方法的頂點宣告來繪製三角形修補程式， [**IDirect3DDevice9：:D rawtripatch**](/windows/desktop/api) 將會失敗。 如需頂點宣告的詳細資訊，請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。

在 DirectX 8.x 中，所謂的順序其實是什麼程度。 在 Direct3D 9 中， [**D3DDEGREETYPE**](./d3ddegreetype.md)的角度現在已指定。


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



度數類型的變更會影響其他兩個結構。


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



驅動程式需要修正編譯錯誤，這些錯誤會在使用新標頭進行編譯時產生此變更。 不需要變更任何功能。

## <a name="adaptive-tessellation"></a>適應性鑲嵌

調適型鑲嵌可以套用至高序位基本專案，包括 N 個修補程式、矩形修補程式和三角形修補程式。 D3DRS ENABLEADAPTIVETESSELLATION 會啟用這項功能 \_ ，並根據眼睛空間中控制頂點的深度值，以自我調整方式 tessellates 修補程式。

Z 座標 (Zi) 的控制項頂點 (Vi) ，其會藉由執行具有4個向量的點乘積來轉換為眼睛空間 (Zieye) ，作為深度值使用。  (使用 D3DRS \_ ADAPTIVETESS \_ X、D3DRS \_ ADAPTIVETESS \_ Y、D3DRS \_ ADAPTIVETESS \_ Z 和 D3DRS \_ ADAPTIVETESS \_ W) 時，應用程式會指定 (Mdm) 的4d 向量。 這個4向量可以是串連世界的第三個數據行，也可以是視圖矩陣。 它也可以用來將刻度套用至 Zieye。

從 Zieye 計算鑲嵌層級 Ti 的函式會假設為 (MaxTessellationLevel/Zieye) ，這表示 MaxTessellationLevel 是在眼睛空間中 Z = 1 的鑲嵌層級。 MaxTessellationLevel 等於 [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) 針對 N 個修補程式所設定的值，若為 RT 修補程式，則等於 pNumSegs。 鑲嵌式層級接著會壓制至值（由兩個額外的轉譯狀態所定義 D3DRS \_ MINTESSELLATIONLEVEL 和 D3DRS \_ MAXTESSELLATIONLEVEL），其定義要壓制至的最小和最大鑲嵌層級。 每個頂點的 Ti 會沿著修補程式的邊緣進行平均，以取得該邊緣的鑲嵌式層級。 針對矩形修補程式、三角形修補程式和 N 修補程式計算 Ti 的演算法，在用來計算鑲嵌層級的控制項頂點上有所不同。

針對具有 B 曲線的矩形修補程式，會使用四個最外層的控制項頂點。 例如，使用 D3DORDER 的 \_ 三階順序：頂點 (1、1) 和 (1 寬度-2) 可搭配 pNumSegs \[ 0 \] 、頂點 (1、寬度-2) 和 (高度-2、高度-2) 搭配 pNumSegs \[ 1 \] 、頂點 (高度-2、寬度-2) 和 (1、寬度-2) 與 pNumSegs 2 搭配使用，而 \[ \] 頂點 (2，1) 和 (1，1) 用於 pNumSegs \[ 3 \] 。

針對三角形修補程式，會使用角落修補程式頂點。 使用 D3DORDER 的 \_ 三階順序：頂點 (0) 和 (9) 會搭配 pNumSegs \[ 0 使用 \] 、頂點 (9) 和 (6) 用於 pNumSegs \[ 1 \] 和頂點 (6) 和 (0) 用於 pNumSegs \[ 3 \] 。

若是 N 個修補程式，則會使用三角形頂點。

針對具有貝塞爾單位的矩形和三角形修補程式，會使用邊角控制頂點。

每個頂點的鑲嵌速率控制。 應用程式可以選擇性地為每個頂點提供單一的固定點浮點值，可用來控制鑲嵌率。 這是使用 D3DDECLUSAGE TESSFACTOR 所提供 \_ ，其使用方式索引必須為0，而輸入類型必須是 D3DDECLTYPE \_ FLOAT1。 這會乘以每個頂點的鑲嵌層級。

### <a name="math"></a>數學

以兩個控制頂點（ (Ve1，Ve2) ）表示的邊緣 e () Te 的鑲嵌層級，其計算方式如下所示：


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



當 D3DRS \_ ENABLEADAPTIVETESSELLATION 為 **TRUE** 時，三角形 (三角形清單、風扇、條紋) 繪製為 N 修補程式， [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) 的設定值小於1.0。

### <a name="api-changes"></a>API 變更

新的呈現狀態：


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



和其預設值：


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



新的硬體 cap：


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點管線](vertex-pipeline.md)
</dt> </dl>

 

 
