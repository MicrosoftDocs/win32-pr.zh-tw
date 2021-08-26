---
title: " (Direct3D 11) 的效果群組語法"
description: 使用本節所述的語法來宣告效果群組。
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c1b2c72b0a67a31911a0f2c9f9ae6ac0e9e20463a850c303dab4a208401d1c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069748"
---
# <a name="effect-group-syntax-direct3d-11"></a> (Direct3D 11) 的效果群組語法

使用本節所述的語法來宣告效果群組。


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a>參數



| 項目                                                                                                                                                                           | 描述                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | equired 關鍵字。<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName<br/>                                                                       | 必要。 可唯一識別效果群組名稱的 ASCII 字串。 不同于技術，群組必須有名稱，以確保技術有唯一的識別碼 (請參閱下面) 的 [群組和技術] 區段。<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < 注釋 ><br/> | \[（ \] 選擇性）。  (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。 如需語法，請參閱 (Direct3D 11) 的批註語法。 <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/>                                           | 可能是 "technique10" 或 "technique11"。 使用 Direct3D 11 的新功能 (5 \_ 0 著色器、BindInterfaces 等) 的技巧必須使用 "technique11"。<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName<br/>                                                       | 選擇性。 可唯一識別效果技巧名稱的 ASCII 字串。 <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>群組和技巧

為了維持與 fx \_ 4 0 效果的相容性 \_ ，群組是選擇性的。 所有全域技術都有隱含的 Null 命名群組。

請考慮下列範例：


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



在 c + + 中，有兩種方式可以依名稱取得技巧。 下列命令會尋找明顯的技巧：


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



為了確保 [**ID3DX11Effect：： GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) 的運作方式類似于效果10，所有定義的群組都必須有名稱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](d3d11-effect-format.md)
</dt> <dt>

[ (Direct3D 11) 的效果技巧語法 ](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





