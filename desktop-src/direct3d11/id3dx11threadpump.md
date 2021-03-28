---
title: 'ID3DX11ThreadPump 介面 (D3DX11core .h) '
description: 執行緒抽取會以非同步方式執行工作。
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- ID3DX11ThreadPump 介面 Direct3D 11
- ID3DX11ThreadPump 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094019"
---
# <a name="id3dx11threadpump-interface"></a>ID3DX11ThreadPump 介面

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

執行緒抽取會以非同步方式執行工作。 它是透過呼叫 [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md)來建立。 有數個 Api 會採用選擇性的執行緒抽取作為參數，例如 [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) 和 [**D3DX11CompileFromFile**](d3dx11compilefromfile.md);如果您將執行緒抽取介面傳遞至這些 Api，函式將會在個別的執行緒上以非同步方式執行。 尤其是在多處理器的電腦上，執行緒抽取可以載入資源並處理資料，而不會明顯降低效能。

## <a name="members"></a>成員

**ID3DX11ThreadPump** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX11ThreadPump** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11ThreadPump** 介面具有這些方法。



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
<td style="text-align: left;"><a href="id3dx11threadpump-addworkitem.md"><strong>Azuretasks</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 將工作專案加入至執行緒抽取。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 取得執行緒抽取內三個佇列中的專案數。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 取得執行緒抽取中的工作專案數。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 在裝置完成載入和處理之後，將工作專案設定為裝置。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 清除執行緒抽取中的所有工作專案。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
</blockquote>
<br/> 等候執行緒抽取中的所有工作專案完成。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

### <a name="using-a-thread-pump"></a>使用執行緒抽取

執行緒抽取會使用下列三個步驟的處理常式來載入和處理資料：

1.  使用 [**資料載入**](id3dx11dataloader.md)器載入和解壓縮資料。 資料載入器物件有三個方法，當執行緒提取在載入和解壓縮資料時，會在內部呼叫： [**ID3DX11DataLoader：： Load**](id3dx11dataloader-load.md)、 [**ID3DX11DataLoader：:D ecompress**](id3dx11dataloader-decompress.md)和 [**ID3DX11DataLoader：:D estroy**](id3dx11dataloader-destroy.md)。 這三個 Api 的特定功能會根據所載入和解壓縮的資料類型而有所不同。 資料載入器介面也可以被繼承，而且如果載入的資料檔是以一個自訂格式來定義，則可以變更其 Api。
2.  使用 [**資料處理器**](id3dx11dataprocessor.md)來處理資料。 資料處理器物件有三個方法，當執行緒在處理資料時，會在內部呼叫： [**ID3DX11DataProcessor：:P rocess**](id3dx11dataprocessor-process.md)、 [**ID3DX11DataProcessor：： CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)和 [**ID3DX11DataProcessor：:D estroy**](id3dx11dataprocessor-destroy.md)。 根據資料的類型而定，處理資料的方式會有所不同。 例如，如果資料是儲存為 JPEG 的材質，則 [**ID3DX11DataProcessor：:P rocess**](id3dx11dataprocessor-process.md) 會執行 JPEG 解壓縮，以取得影像的原始影像位。 如果資料是著色器，則 [**ID3DX11DataProcessor：:P rocess**](id3dx11dataprocessor-process.md) 會將 HLSL 編譯成位元組程式碼。 處理資料之後，將會針對該資料 (使用 [**ID3DX11DataProcessor：：) CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md) 建立裝置物件，並將該物件新增至裝置物件的佇列。 您也可以繼承資料處理器介面，如果其中一個應用程式的 Api 是以一個自訂格式來處理的資料檔案，則可以變更其 Api。
3.  將裝置物件系結至裝置。 當其中一個應用程式呼叫 ID3DX11ThreadPump 時，就會執行此動作 [**：:P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md)，這會將裝置物件佇列中指定的物件數目系結至裝置。

執行緒抽取可以用兩種方式之一來載入資料：藉由呼叫接受執行緒提取的 API 做為參數，例如 [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) 和 [**D3DX11CompileFromFile**](d3dx11compilefromfile.md)，或呼叫 [**ID3DX11ThreadPump：： azuretasks**](id3dx11threadpump-addworkitem.md)。 如果是採用執行緒抽取的 Api，則會在內部建立資料載入器和資料處理器。 在 Azuretasks 的案例中，資料載入器和資料處理器必須事先建立，然後再傳遞至 Azuretasks。 D3DX11 提供一組 Api，可用來建立可載入和處理一般資料格式的資料載入器和資料處理器。 針對自訂資料格式，必須繼承資料載入器和資料處理器介面，而且必須重新定義它們的方法。

執行緒抽取物件佔用大量的資源，因此通常每個應用程式只能建立一個資源。

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

 

