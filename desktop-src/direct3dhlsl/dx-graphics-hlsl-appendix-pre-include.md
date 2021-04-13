---
title: " include 指示詞"
description: 預處理器指示詞，可將指定檔案的內容插入來來源程式中指示詞出現的位置。
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- include 指示詞 HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990942"
---
# <a name="include-directive"></a>\#include 指示詞

預處理器指示詞，可將指定檔案的內容插入來來源程式中指示詞出現的位置。


| \#包含 "*filename*"       |
|------------------------------|
| \#包含 <*檔案名*> |

## <a name="parameters"></a>參數

| 項目 | 描述 |
|------|-------------|
| *filename* | 要包含之檔案的檔案名（選擇性地在前面加上目錄規格）。 檔案名必須指定現有的檔案。 |

## <a name="remarks"></a>備註

\#Include 指示詞會導致指定檔案的整個內容取代指示詞。 當預處理器找到具有指定名稱的檔案時，就會立即停止搜尋;如果您為檔案指定完整、明確的路徑規格，預處理器只會搜尋指定的路徑。

> [!NOTE]
> [效果編譯器工具](/windows/desktop/direct3dtools/fxc)具有使用/i 參數的內建 include 處理常式。 不過，從 API 執行編譯器時，您可以藉由執行 ID3DXInclude 介面提供自訂的 include 處理常式。

這兩種語法形式之間的差異在於，當路徑未完成指定時，預處理器會搜尋標頭檔的順序，如下表所示。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>語法形式</th>
<th>預處理器搜尋模式</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#包含 <b>&quot;</b> <em>檔案名</em><b>&quot;</b></td>
<td>搜尋 include 檔：
<ol>
<li>在與包含 #include 指示詞的檔案相同的目錄中。</li>
<li>在包含 #include 指示詞之檔案的 #include 指示詞之任何檔案的目錄中。</li>
<li>在/I 編譯器選項指定的路徑中，依列出的順序排列。</li>
<li><p>在 INCLUDE 環境變數所指定的路徑中，依列出的順序排列。</p>
<blockquote>
[!NOTE]<br />
在開發環境中會忽略 INCLUDE 環境變數。 請參閱您開發環境的檔，以取得如何設定專案包含路徑的相關資訊。
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#包含 <b><</b> <em>檔案名</em><b>></b></td>
<td>搜尋 include 檔：
<ol>
<li>在/I 編譯器選項指定的路徑中，依列出的順序排列。</li>
<li><p>在 INCLUDE 環境變數所指定的路徑中，依列出的順序排列。</p>
<blockquote>
[!NOTE]<br />
在開發環境中會忽略 INCLUDE 環境變數。 請參閱您開發環境的檔，以取得如何設定專案包含路徑的相關資訊。
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>範例

下列範例會讓預處理器將 include 指示詞取代為 \# stdio.h 的內容。 因為此範例使用角括弧格式，預處理器只會在/I 編譯器選項和 INCLUDE 環境變數所列的目錄中搜尋檔案。

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>另請參閱

- [ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)

- [ID3D10Include 介面](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [效果-編譯器工具](/windows/desktop/direct3dtools/fxc)