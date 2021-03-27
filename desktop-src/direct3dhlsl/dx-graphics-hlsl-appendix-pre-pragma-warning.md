---
title: warning pragma 指示詞
description: 修改編譯器警告訊息行為的 Pragma 指示詞。
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- 警告 pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932696"
---
# <a name="warning-pragma-directive"></a>warning pragma 指示詞

修改編譯器警告訊息行為的 Pragma 指示詞。



| \#pragma 警告 ( *警告-規範* ： *警告-數位-清單* \[ ; *警告-規範* ： *警告-數位-清單*... \] )  |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a>參數



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>項目</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-規範</em><br/></td>
<td>要針對指定的警告設定的行為。 此參數可以採用下表所列的其中一個值。 <br/> 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>once</td>
<td>只顯示指定數位一次的警告訊息。</td>
</tr>
<tr class="even">
<td>預設</td>
<td>將具有指定數位之警告的行為重設為其預設值。 這也具有開啟警告的效果（預設為關閉）。 警告會在其預設層級產生。</td>
</tr>
<tr class="odd">
<td>1、2、3、4</td>
<td>將指定的層級套用至具有指定數位的警告。 這也具有開啟警告的效果（預設為關閉）。</td>
</tr>
<tr class="even">
<td>disable</td>
<td>請勿發出具有指定數位的警告。</td>
</tr>
<tr class="odd">
<td>error</td>
<td>以指定的數位將警告報告為錯誤。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>警告-數位-清單</em></p></td>
<td><p>以空格分隔的清單，其中列出要修改其行為的警告數目。</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

您可以使用分號分隔變更，在相同的警告 pragma 內指定任何數目的相異警告行為變更。

編譯器會將4000加入至0和999之間的任何警告編號。 若為大於4699的警告編號， (與程式碼產生相關聯的警告編號) 警告 pragma 只有在放置於函式定義之外時才會生效。 如果指定的數位大於4699，並在函式內使用，則會忽略 pragma。

HLSL 警告 pragma 不支援 c + + 編譯器中包含的 warning pragma 的 **push** 和 **pop** 功能。

## <a name="examples"></a>範例

下列範例會停用警告4507和4034、顯示警告4385一次，並將警告4164報告為錯誤。


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



上述範例在功能上等同于下列專案：


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\# (DirectX HLSL) 的 pragma 指示詞 ](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





