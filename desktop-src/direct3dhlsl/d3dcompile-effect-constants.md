---
title: 'D3DCOMPILE_EFFECT 常數 (D3DCompiler) '
description: 這些常數會指示編譯器編譯效果檔案的方式，或執行時間處理效果檔案的方式。
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d5c31efb17d2f852ac3903a5946ce5fb72fcef86ef083c474328859472c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286912"
---
# <a name="d3dcompile_effect-constants"></a>D3DCOMPILE \_ 效果常數

這些常數會指示編譯器編譯效果檔案的方式，或執行時間處理效果檔案的方式。

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE \_ 效果 \_ 子 \_ 效果**
</dt> <dd> <dl> <dt>

 (1 << 0) 
</dt> <dt>



將 ( 的效果編譯) 的子效果。 子效果沒有任何共用值的初始化運算式，因為這些子效果會在效果集區)  (的主要效果中初始化。

> [!Note]  
> 效果集區受到效果 10 (FX10) 的支援，但不受效果 11 (FX11) 。 如需 Direct3D 10 中效果集區與 Direct3D 11 中效果群組之間差異的詳細資訊，請參閱效果集區 [和群組](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences)。

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ 效果 \_ 允許 \_ 緩慢的 \_ OPS**
</dt> <dd> <dl> <dt>

 (1 << 1) 
</dt> <dt>



停用效能模式，並允許可變狀態物件。

預設會啟用效能模式。 效能模式防止非常值運算式出現在狀態物件定義中，因此不允許可變動狀態物件。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DCompiler。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DCompiler 常數](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

