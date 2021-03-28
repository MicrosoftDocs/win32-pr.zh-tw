---
title: texldl-ps
description: 使用特定取樣器來取樣材質。 要取樣的特定 mipmap 詳細資料層級必須指定為紋理座標的第四個元件。 |texldl-ps
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973941"
---
# <a name="texldl---ps"></a>texldl-ps

使用特定取樣器來取樣材質。 要取樣的特定 mipmap 詳細資料層級必須指定為紋理座標的第四個元件。

## <a name="syntax"></a>Syntax



| texldl dst、src0、src1 |
|------------------------|



 

其中：

-   dst 是目的地註冊。
-   src0 是一種來源暫存器，可提供紋理範例的材質座標。 請參閱 [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)。
-   src1 會識別來源取樣器 (s \#) ，其中 \# 指定要取樣的材質取樣器數目。 取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) 列舉所定義的材質和控制項狀態相關聯 (例如 D3DSAMP \_ MINFILTER) 。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

texldl 會在 src1 所參考的取樣器階段上查閱材質集。 詳細資料層級是從 src0 中選取的。 這個值可以是負數，在這種情況下，選取的詳細資料層級就是第零個與 MAGFILTER)  (最大的地圖。 由於 src0 是浮點值，因此如果 MIPFILTER 是兩個 mip 層級之間的線性) ，則會使用小數值來插入 (。 取樣器狀態會接受 MIPMAPLODBIAS 和 MAXMIPLEVEL。 如需取樣器狀態的詳細資訊，請參閱 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)。

如果著色器程式是從沒有紋理集的取樣器取樣，則會在目的地暫存器中取得0001。

以下是參考裝置所遵循的粗略演算法：


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



限制：

-   材質座標不應以紋理大小進行縮放。
-   dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 。
-   dst 可以接受 writemask。 請參閱 [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)。
-   遺漏元件的預設值為0或1，並取決於材質格式。
-   src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# 。 src1 可能不會使用否定修飾詞 (請參閱 [目的地登錄寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)) 。 src1 可能會使用 swizzle (請參閱 [來源登錄 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)) ，這會在取樣之後套用，但在寫入遮罩 (上，請參閱) 接受的目的地登錄寫入遮罩。 您必須使用 [ \_ samplerType (sm2、sm3-ps asm) ](dcl-samplertype---ps.md)) 在著色器的開頭 (宣告取樣器。
-   執行材質範例所需的座標數目取決於取樣器的宣告方式。 如果它宣告為 cube，則需要三個元件的材質座標 ( rgb) 。 驗證會強制為 tex ldl 提供的座標，足以滿足針對取樣器宣告的 \_ 材質維度。 但是，不保證應用程式實際上會透過 API) 來設定材質 (，其維度等於針對取樣器宣告的維度。 在這種情況下，執行時間會嘗試偵測不相符的 (可能只有) 的 debug。 系統會允許和紋理座標中具有較少維度的材質進行取樣，並假設忽略額外的材質座標元件。 相反地，針對材質座標中有多個維度的材質進行取樣，是不合法的。
-   如果 src0 (材質座標) 是 [暫時性](dx9-graphics-reference-asm-ps-registers-temporary.md)暫存器，則必須先撰寫查閱 (所需的元件) 。
-   取樣不帶正負號的 RGB 材質將會產生介於0.0 到1.0 之間的 float 值。
-   取樣帶正負號的材質會導致介於-1.0 到1.0 之間的浮點值。
-   取樣浮點數材質時，Float16 表示資料將在 MAX Float16 內的範圍內 \_ 。 Float32 表示將會使用管線的最大範圍。 在任一範圍之外取樣都未定義。
-   沒有相依的讀取限制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
