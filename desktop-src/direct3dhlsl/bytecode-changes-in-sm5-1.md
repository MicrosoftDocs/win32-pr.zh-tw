---
title: SM 5.1 的位元組位元組變更
description: SM 5.1 變更如何在指示中宣告和參考資源暫存器。
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d66db788b0012a1c3221e37d4c2dd4e41566c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311619"
---
# <a name="bytecode-changes-in-sm51"></a>SM 5.1 的位元組位元組變更

SM 5.1 變更如何在指示中宣告和參考資源暫存器。

SM 5.1 會向宣告註冊「變數」，類似于如何針對群組共用記憶體暫存器完成這項工作，如下列範例所示：

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

此範例的反組譯如下：

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim Space Slot  Elements
// ------------------------------ ---------- ------- ----------- ----- ---- ---------
// samp0                             sampler      NA          NA     0    5         1
// tex0                              texture  float4          2d     0    5         1
// tex1[0][5][3]                     texture  float4          2d     0   10 unbounded
// tex2[8]                           texture  float4          2d     1    0         8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots used
```

每個著色器資源範圍現在都有一個識別碼， (著色器位元組程式碼中) 的名稱。 例如，在著色器位元組程式碼中，tex1 材質陣列變成不是1。 將唯一識別碼提供給每個資源範圍，可提供兩個專案：

-   明確識別哪些資源範圍 (請參閱 \_ \_) 的指令索引 (查看範例指示) 。
-   將屬性集附加至宣告，例如元素類型、跨距大小、點陣作業模式等。

請注意，範圍的識別碼與 HLSL 下限宣告沒有關聯。

反映資源系結和著色器宣告指示的順序，是協助識別 HLSL 變數和位元組程式碼識別碼之間的對應。

SM 5.1 中的每個宣告指令都使用3D 運算元來定義：範圍識別碼、下限和上限。 發出額外的權杖來指定註冊空間。 可能也會發出其他標記，以傳達範圍的其他屬性，例如，cbuffer 或結構化的緩衝區宣告指令會發出 cbuffer 或結構的大小。 您可以在 d3d12TokenizedProgramFormat 和 D3D10ShaderBinary：： CShaderCodeParser 中找到編碼的確切詳細資料。

SM 5.1 指示將不會發出額外的資源運算元資訊做為指令 (的一部分，如同 SM 5.0) 。 此資訊現在已移至宣告指示。 在 SM 5.0 中，為資源編制索引所需的資源屬性必須在擴充的 opcode 權杖中描述，因為索引將關聯性模糊至宣告。 在 SM 5.1 中，每個識別碼 (例如 ' t 1 ' ) 明確地與單一宣告相關聯，以描述必要的資源資訊。 因此，不會再發出用來描述資源資訊之指示的延伸操作碼權杖。

在非宣告的指示中，取樣器、SRVs 和 UAVs 的資源運算元是2D 運算元。 第一個索引是指定範圍識別碼的常值常數。 第二個索引代表索引的 linearized 值。 相對於對應的登錄空間的開頭，會計算此值， (不是相對於邏輯範圍的開頭) 為了讓與根簽章更好的相互關聯，以及降低調整索引的驅動程式編譯器負擔。

CBVs 的資源運算元是3D 運算元：範圍的常值識別碼、cbuffer 的索引，以及特定 cbuffer 實例的位移。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型5。1](shader-model-5-1.md)
</dt> </dl>

 

 




