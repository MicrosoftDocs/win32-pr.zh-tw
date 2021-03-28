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
# <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="dde50-103">SM 5.1 的位元組位元組變更</span><span class="sxs-lookup"><span data-stu-id="dde50-103">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="dde50-104">SM 5.1 變更如何在指示中宣告和參考資源暫存器。</span><span class="sxs-lookup"><span data-stu-id="dde50-104">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span>

<span data-ttu-id="dde50-105">SM 5.1 會向宣告註冊「變數」，類似于如何針對群組共用記憶體暫存器完成這項工作，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="dde50-105">SM5.1 moves towards declaring a register “variable”, similar to how it is done for group shared memory registers, illustrated by the following example:</span></span>

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

<span data-ttu-id="dde50-106">此範例的反組譯如下：</span><span class="sxs-lookup"><span data-stu-id="dde50-106">The disassembly of this example follows:</span></span>

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

<span data-ttu-id="dde50-107">每個著色器資源範圍現在都有一個識別碼， (著色器位元組程式碼中) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dde50-107">Each shader resource range now has an ID (a name) in the shader bytecode.</span></span> <span data-ttu-id="dde50-108">例如，在著色器位元組程式碼中，tex1 材質陣列變成不是1。</span><span class="sxs-lookup"><span data-stu-id="dde50-108">For example, tex1 texture array becomes ‘t1’ in the shader byte code.</span></span> <span data-ttu-id="dde50-109">將唯一識別碼提供給每個資源範圍，可提供兩個專案：</span><span class="sxs-lookup"><span data-stu-id="dde50-109">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="dde50-110">明確識別哪些資源範圍 (請參閱 \_ \_) 的指令索引 (查看範例指示) 。</span><span class="sxs-lookup"><span data-stu-id="dde50-110">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="dde50-111">將屬性集附加至宣告，例如元素類型、跨距大小、點陣作業模式等。</span><span class="sxs-lookup"><span data-stu-id="dde50-111">Attach set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc..</span></span>

<span data-ttu-id="dde50-112">請注意，範圍的識別碼與 HLSL 下限宣告沒有關聯。</span><span class="sxs-lookup"><span data-stu-id="dde50-112">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="dde50-113">反映資源系結和著色器宣告指示的順序，是協助識別 HLSL 變數和位元組程式碼識別碼之間的對應。</span><span class="sxs-lookup"><span data-stu-id="dde50-113">The order of reflection resource bindings and shader declaration instructions is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="dde50-114">SM 5.1 中的每個宣告指令都使用3D 運算元來定義：範圍識別碼、下限和上限。</span><span class="sxs-lookup"><span data-stu-id="dde50-114">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="dde50-115">發出額外的權杖來指定註冊空間。</span><span class="sxs-lookup"><span data-stu-id="dde50-115">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="dde50-116">可能也會發出其他標記，以傳達範圍的其他屬性，例如，cbuffer 或結構化的緩衝區宣告指令會發出 cbuffer 或結構的大小。</span><span class="sxs-lookup"><span data-stu-id="dde50-116">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="dde50-117">您可以在 d3d12TokenizedProgramFormat 和 D3D10ShaderBinary：： CShaderCodeParser 中找到編碼的確切詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dde50-117">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and D3D10ShaderBinary::CShaderCodeParser.</span></span>

<span data-ttu-id="dde50-118">SM 5.1 指示將不會發出額外的資源運算元資訊做為指令 (的一部分，如同 SM 5.0) 。</span><span class="sxs-lookup"><span data-stu-id="dde50-118">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="dde50-119">此資訊現在已移至宣告指示。</span><span class="sxs-lookup"><span data-stu-id="dde50-119">This information is now moved to the declaration instructions.</span></span> <span data-ttu-id="dde50-120">在 SM 5.0 中，為資源編制索引所需的資源屬性必須在擴充的 opcode 權杖中描述，因為索引將關聯性模糊至宣告。</span><span class="sxs-lookup"><span data-stu-id="dde50-120">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="dde50-121">在 SM 5.1 中，每個識別碼 (例如 ' t 1 ' ) 明確地與單一宣告相關聯，以描述必要的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="dde50-121">In SM5.1 each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="dde50-122">因此，不會再發出用來描述資源資訊之指示的延伸操作碼權杖。</span><span class="sxs-lookup"><span data-stu-id="dde50-122">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="dde50-123">在非宣告的指示中，取樣器、SRVs 和 UAVs 的資源運算元是2D 運算元。</span><span class="sxs-lookup"><span data-stu-id="dde50-123">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="dde50-124">第一個索引是指定範圍識別碼的常值常數。</span><span class="sxs-lookup"><span data-stu-id="dde50-124">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="dde50-125">第二個索引代表索引的 linearized 值。</span><span class="sxs-lookup"><span data-stu-id="dde50-125">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="dde50-126">相對於對應的登錄空間的開頭，會計算此值， (不是相對於邏輯範圍的開頭) 為了讓與根簽章更好的相互關聯，以及降低調整索引的驅動程式編譯器負擔。</span><span class="sxs-lookup"><span data-stu-id="dde50-126">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="dde50-127">CBVs 的資源運算元是3D 運算元：範圍的常值識別碼、cbuffer 的索引，以及特定 cbuffer 實例的位移。</span><span class="sxs-lookup"><span data-stu-id="dde50-127">A resource operand for CBVs is a 3D operand: literal ID of the range, index of the cbuffer, offset into the particular instance of cbuffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dde50-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="dde50-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dde50-129">適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能</span><span class="sxs-lookup"><span data-stu-id="dde50-129">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="dde50-130">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="dde50-130">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> </dl>

 

 




