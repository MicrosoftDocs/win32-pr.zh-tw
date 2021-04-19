---
description: 傳遞至 TraceRay 函式的旗標，可覆寫透明度、剔除和早期輸出行為。
ms.assetid: ''
title: RAY_FLAG 列舉
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973784"
---
# <a name="ray_flag-enumeration"></a>光線 \_ 旗標列舉

傳遞至 [**TraceRay**](traceray-function.md) 函式的旗標，可覆寫透明度、剔除和早期輸出行為。

## <a name="syntax"></a>Syntax


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**光線 \_ 旗標 \_ 無**
</dt> <dd>

未選取任何選項。

</dd> <dt>

<span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**光線 \_ 旗標 \_ 強制不 \_ 透明**
</dt> <dd>

Raytrace 中遇到的所有光線基本交集都會視為不透明。  因此，不論點擊幾何是否指定 D3D12 \_ RAYTRACING \_ 幾何 \_ 旗 \_ 標不透明，以及叫用實例上的實例旗標為何，都不會執行任何的點擊著色器。

此旗標與光線旗標 \_ 互斥 \_ ，會強制 \_ 非 \_ 透明、光線 \_ 旗標挑選不透明， \_ \_ 而光線旗標則 \_ \_ 挑選 \_ 非不 \_ 透明。


</dd> <dt>

<span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**光線 \_ 旗標 \_ 強制 \_ 非 \_ 透明**
</dt> <dd>

在 raytrace 中遇到的所有光線基本型交集都會視為不透明。  如此一來，不論點擊幾何是否指定 D3D12 \_ RAYTRACING \_ 幾何 \_ 旗 \_ 標不透明，而且不論點擊的實例上是否有實例旗標，都會執行任何的點擊著色器。
此旗標與光線旗標 \_ 互斥 \_ FORCE_ \OPAQUE，光線 \_ 旗標 \_ 挑選 \_ 不透明，而光線旗標則 \_ \_ 挑選 \_ 非不 \_ 透明。


</dd> <dt>

<span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**光線 \_ 旗標 \_ 接受 \_ 第一個 \_ 點擊 \_ 和 \_ 結束 \_ 搜尋**
</dt> <dd>

在 raytrace 中遇到的第一個光線基本交集會自動導致 **AcceptHitAndEndSearch** 在任何點擊著色器之後立即呼叫，包括是否沒有任何點擊著色器。 
 
唯一的例外狀況是在上述任何叫用著色器呼叫 **IgnoreHit** 時，在此情況下，光線會繼續受到影響，讓下一個點擊變成另一個候選項成為第一個叫用。  若要套用此例外狀況，必須實際執行任何點擊著色器。  因此，如果略過任何叫用著色器，因為叫用視為不透明的 (例如，因為光線旗標會強制不透明 \_ \_ \_ 或 D3D12 \_ RAYTRACING \_ 幾何旗標不 \_ \_ 透明或 D3D12 RAYTRACING 實例) 旗標不透明或 \_ 實例旗標不透明 \_ \_ \_ ，則會呼叫 **AcceptHitAndEndSearch** 。

如果最接近的點擊著色器出現在第一個點擊，則會叫用它，除非光線 \_ 旗標 \_ 略過 \_ 最接近的 \_ 點擊 \_ 著色器也存在。  所找到的某個點擊會被視為「最接近」，即使可能已接近光線的其他潛在點擊可能還沒被造訪過也是一樣。

此旗標的一般用法是用於陰影，其中只需要找到單一點擊。


</dd> <dt>

<span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**光線 \_ 旗標 \_ 略過 \_ 最接近的 \_ 點擊 \_ 著色器**
</dt> <dd>

即使至少有一個叫用，且最接近的點擊群組包含最接近的點擊著色器，也會略過該著色器的執行。 

</dd> <dt>

<span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**光線 \_ 旗 \_ 標 \_ 挑選 \_ 朝上 \_ 三角形**
</dt> <dd>

啟用向後三角形的剔除。 請參閱 **D3D12 \_ RAYTRACING \_ 實例 \_ 旗標** ，以針對每個實例來選取要來回的三角形。

在指定 D3D12 \_ RAYTRACING \_ 實例旗標三角形挑選停用的實例上 \_ \_ \_ \_ ，此旗標不會有任何作用。

在 D3D12 RAYTRACING geometry 型別三角形以外的幾何類型上 \_ \_ \_ \_ ，此旗標沒有任何作用。

此旗標與光線旗標 \_ \_ 挑選 \_ 正面三角形 \_ 互斥 \_ 。


</dd> <dt>

<span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**光線 \_ 旗標 \_ 挑選 \_ 正面的 \_ \_ 三角形**
</dt> <dd>

啟用對等三角形的挑選。 請參閱 **D3D12 \_ RAYTRACING \_ 實例 \_ 旗標** ，以針對每個實例來選取要來回的三角形。

在指定 D3D12 \_ RAYTRACING \_ 實例旗標三角形挑選停用的實例上 \_ \_ \_ \_ ，此旗標不會有任何作用。

在 D3D12 RAYTRACING geometry 型別三角形以外的幾何類型上 \_ \_ \_ \_ ，此旗標沒有任何作用。

此旗標與光線旗標 \_ \_ 挑選 \_ 回 \_ 三角形 \_ 的互斥。


</dd> <dt>

<span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**光線 \_ 旗標 \_ 挑選不 \_ 透明**
</dt> <dd>

根據幾何和實例旗標，選出被視為不透明的所有基本專案。

此旗標互斥于光線 \_ 旗標 \_ ：強制不透明 \_ 、光線 \_ 旗標 \_ 強制 \_ 非 \_ 透明，而光線 \_ 旗標 \_ 挑選 \_ 非不 \_ 透明。


</dd> <dt>

<span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**光線 \_ 旗標 \_ 挑選 \_ 非 \_ 透明**
</dt> <dd>

根據幾何和實例旗標，選出被視為不透明的所有基本專案。

此旗標與光線旗標 \_ 互斥 \_ \_ 、光線旗標 \_ \_ 強制 \_ 非 \_ 透明，而光線旗標挑選 \_ \_ \_ 不透明。


</dd>

## <a name="requirements"></a>規格需求



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




