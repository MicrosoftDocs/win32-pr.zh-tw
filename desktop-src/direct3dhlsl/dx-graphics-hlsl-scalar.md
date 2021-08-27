---
title: 純量類型
description: 純量類型
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- 純量類型 HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7ddfbc679d95ca0a2c6fce0710b5de37f677fe0f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626724"
---
# <a name="scalar-types"></a>純量類型


HLSL 支援數個純量資料類型：

-   **bool** -true 或 false。
-   **int** -32-位帶正負號的整數。
-   **uint** -32-bit 不帶正負號整數。
-   **dword** -32-位不帶正負號整數。
-   **半** 16 位浮點值。 這種資料類型只提供語言相容性。 Direct3D 10 著色器目標會將所有的半資料類型對應至 float 資料類型。 如果) 需要這項功能，就不能在統一全域變數上使用半資料類型 (使用/Gec 旗標。
-   **float** -32 位浮點值。
-   **雙** 64 位浮點值。 您無法使用雙精確度值做為資料流程的輸入和輸出。 若要在著色器之間傳遞雙精確度值，請將每個 **double** 宣告為一對 **uint** 資料類型。 然後，使用 [**asuint**](asuint.md) 函式將每個 **雙** 精確度封裝到 **uint** 的配對，並使用 [**asdouble**](asdouble.md) 函式將一組 **uint** 重新包裝回 **雙精度浮點數**。

從 Windows 8 HLSL 開始也支援最小有效位數純量資料類型。 圖形驅動程式可以使用大於或等於指定位精確度的精確度，來執行最小有效位數純量資料類型。 建議您不要依賴相依于特定基礎精確度的固定或換行行為。 例如，圖形驅動程式可能會以完整的32位有效位數執行 **min16float** 值的算數運算。

-   **min16float** -最小16位浮點值。
-   **min10float** -最小的10位浮點值。
-   **min16int** -最小16位帶正負號的整數。
-   **min12int** -最小12位帶正負號的整數。
-   **min16uint** -最小16位不帶正負號整數。

如需純量常值的詳細資訊，請參閱 [文法](dx-graphics-hlsl-appendix-grammar.md)。



<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 10 之間的差異：<br/> 在 Direct3D 10 中，下列類型是 float 類型的修飾詞。<br/>
<ul>
<li><strong>snorm 浮點數</strong> - IEEE 32 位帶正負號的標準化浮點數，範圍介於-1 到1（含）之間。</li>
<li><strong>unorm 浮點數</strong> - IEEE 32 位不帶正負號-在範圍0到1（含）的標準化浮點數。</li>
</ul>
例如，以下是4個元件的已簽署標準化浮點變數宣告。<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a>字串類型

HLSL 也支援 **字串** 類型，也就是 ASCII 字串。 沒有可接受字串的作業或狀態，但效果可以查詢字串參數和批註。

## <a name="example"></a>範例

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a>另請參閱



* [宣告純量類型](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
