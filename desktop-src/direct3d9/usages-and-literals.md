---
description: 用法類似于參數的範圍，因為它會定義參數有效的範圍。
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: " (Direct3D 9) 的使用方式和常值"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971945"
---
# <a name="usages-and-literals-direct3d-9"></a> (Direct3D 9) 的使用方式和常值

用法類似于參數的範圍，因為它會定義參數有效的範圍。



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 值  | 描述                                                                                                                                                                                                                                                                         |
| const  | 參數在所有函式的範圍內都是常數。  (請注意，這類參數仍然可以使用 [**ID3DXEffect**](id3dxeffect.md) 或 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)寫入，因為這會發生在所有函數的範圍之外。 )  |
| 共用 | 此參數將會在效果集區中共用。                                                                                                                                                                                                                                    |
| static | 應用程式不會看到參數，也就是您無法從 [**ID3DXEffect**](id3dxeffect.md) 或 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)存取。                                                                                                  |



 

將參數標記為常值表示它的值永遠不會變更。 這可讓效果編譯器進行額外的優化。

只有非共用的最上層參數可以標記為常值。 參數只能使用 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)標示為常值。 無法使用 [**ID3DXEffect**](id3dxeffect.md)來設定常值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



