---
title: 'ID3DX11DataProcessor 介面 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 ID3DX11ThreadPump 介面用來以非同步方式載入資料的資料處理物件。
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- ID3DX11DataProcessor 介面 Direct3D 11
- ID3DX11DataProcessor 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e421a6e840665220311e5a27c0692cd7f347e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104971860"
---
# <a name="id3dx11dataprocessor-interface"></a>ID3DX11DataProcessor 介面

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

[**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)用來以非同步方式載入資料的資料處理物件。

## <a name="members"></a>成員

**ID3DX11DataProcessor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX11DataProcessor** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11DataProcessor** 介面具有這些方法。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">方法</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 建立裝置物件。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataprocessor-destroy.md"><strong>摧毀</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 在工作專案完成後損毀處理器。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataprocessor-process.md"><strong>處理序</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 處理資料。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

可以繼承這個物件，並重新定義其成員以處理自訂檔案格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

