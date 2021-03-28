---
title: 'D3DX 介面 (Direct3D 11 圖形) '
description: 本章節包含 D3DX 公用程式程式庫所提供之元件物件模型 (COM) 介面的參考資訊。
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- D3DX 介面，Direct3D 11
- 介面，Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2890c3c55d1bac9eba09c046927e432b1a27f8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024415"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>D3DX 介面 (Direct3D 11 圖形) 

本章節包含 D3DX 公用程式程式庫所提供之元件物件模型 (COM) 介面的參考資訊。

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 


## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> <a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump 介面</strong></a>用來以非同步方式載入資料的資料載入物件。<br/></td>
</tr>
<tr class="even">
<td><a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> <a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump 介面</strong></a>用來以非同步方式載入資料的資料處理物件。<br/></td>
</tr>
<tr class="odd">
<td><a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 執行緒抽取會以非同步方式執行工作。 它是透過呼叫 <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a>來建立。 有數個 Api 會採用選擇性的執行緒抽取作為參數，例如 <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> 和 <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>;如果您將執行緒抽取介面傳遞至這些 Api，函式將會在個別的執行緒上以非同步方式執行。 尤其是在多處理器的電腦上，執行緒抽取可以載入資源並處理資料，而不會明顯降低效能。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX 11 參考](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





