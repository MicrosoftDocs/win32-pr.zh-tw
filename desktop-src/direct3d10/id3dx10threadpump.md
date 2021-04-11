---
description: 用來以非同步方式執行工作，並使用 D3DX10CreateThreadPump 建立。
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: 'ID3DX10ThreadPump 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9fe3f0ca5955963864ef18de5d86fe03083d3f3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116297"
---
# <a name="id3dx10threadpump-interface"></a>ID3DX10ThreadPump 介面

用來以非同步方式執行工作，並使用 [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md)建立。 有幾個 D3DX10 Api 可以選擇性地採用執行緒抽取作為參數，例如 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 和 [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (查看完整清單) 的備註。 如果執行緒抽取傳遞至這些 Api，則會以非同步方式在不同的執行緒抽取執行緒上執行。 這樣做的優點是，它可以讓載入和處理大量資料，而不會在螢幕上看到明顯變慢的效能。

## <a name="members"></a>成員

**ID3DX10ThreadPump** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX10ThreadPump** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX10ThreadPump** 介面具有這些方法。



| 方法                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Azuretasks**](id3dx10threadpump-addworkitem.md)                       | 將工作專案加入至執行緒抽取。<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetQueueStatus**](id3dx10threadpump-getqueuestatus.md)                 | 取得執行緒抽取內三個佇列中的專案數。<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**GetWorkItemCount**](id3dx10threadpump-getworkitemcount.md)             | 取得目前線上程抽取中的工作專案數。<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**ProcessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md) | 在裝置完成載入和處理之後，將工作專案設定為裝置。 當執行緒抽取完成載入和處理資源或著色器時，它會將其保留在佇列中，直到呼叫此 API 為止，此時已處理的專案將會設定為裝置。 這對於控制每個畫面系將資源系結至裝置所花費的處理量相當有用。 請參閱＜備註＞。<br/> |
| [**PurgeAllItems**](id3dx10threadpump-purgeallitems.md)                   | 清除執行緒抽取中的所有工作專案。<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**WaitForAllItems**](id3dx10threadpump-waitforallitems.md)               | 等候執行緒抽取中的所有工作專案完成。<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>備註

執行緒抽取會在三個步驟程式中載入及處理資料。 它會：

1.  使用資料載入器載入和解壓縮資料。 資料載入器物件有三個方法，當執行緒提取在載入和解壓縮資料時，會在內部呼叫： [**ID3DX10DataLoader：： Load**](id3dx10dataloader-load.md)、 [**ID3DX10DataLoader：:D ecompress**](id3dx10dataloader-decompress.md)和 [**ID3DX10DataLoader：:D estroy**](id3dx10dataloader-destroy.md)。 這三個 Api 的特定功能會根據所載入和解壓縮的資料類型而有所不同。 資料載入器介面也可以被繼承，而且如果載入的資料檔是以一個自訂格式來定義，則可以變更其 Api。
2.  使用資料處理器來處理資料。 資料處理器物件有三個方法，當執行緒在處理資料時，會在內部呼叫： [**ID3DX10DataProcessor：:P rocess**](id3dx10dataprocessor-process.md)、 [**ID3DX10DataProcessor：： CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md)和 [**ID3DX10DataProcessor：:D estroy**](id3dx10dataprocessor-destroy.md)。 根據資料的類型而定，處理資料的方式會有所不同。 例如，如果資料是儲存為 JPEG 的材質，則 **ID3DX10DataProcessor：:P rocess** 會執行 JPEG 解壓縮，以取得影像的原始影像位。 如果資料是著色器，則 **ID3DX10DataProcessor：:P rocess** 會將 HLSL 編譯成位元組程式碼。 處理資料之後，將會針對該資料 (使用 **ID3DX10DataProcessor：：) CreateDeviceObject** 建立裝置物件，並將該物件新增至裝置物件的佇列。 您也可以繼承資料處理器介面，如果其中一個應用程式的 Api 是以一個自訂格式來處理的資料檔案，則可以變更其 Api。
3.  將裝置物件系結至裝置。 當其中一個應用程式呼叫 ID3DX10ThreadPump 時，就會執行此動作 [**：:P rocessdeviceworkitems**](id3dx10threadpump-processdeviceworkitems.md)，這會將裝置物件佇列中指定的物件數目系結至裝置。

執行緒抽取可以用兩種方式之一來載入資料：藉由呼叫接受執行緒提取的 API 做為參數，例如 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 和 [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)，或呼叫 [**ID3DX10ThreadPump：： azuretasks**](id3dx10threadpump-addworkitem.md)。 如果是採用執行緒抽取的 Api，則會在內部建立資料載入器和資料處理器。 在 **azuretasks** 的案例中，資料載入器和資料處理器必須事先建立，然後再傳遞至 azuretasks。 D3DX10 提供一組 Api 來建立資料載入器和資料處理器，這些資料載入器和資料處理器都有載入和處理一般資料格式的功能 (請參閱) 的 Api 完整清單的備註。 針對自訂資料格式，必須繼承資料載入器和資料處理器介面，而且必須重新定義它們的方法。

執行緒抽取物件佔用大量的資源，因此通常每個應用程式只能建立一個資源。

內建的 D3DX10 資料載入器



|                                                                            |                                          |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | 以非同步方式建立檔案載入器。     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | 以非同步方式建立資料載入器。     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | 以非同步方式建立資源載入器。 |



 

內建的 D3DX10 資料處理器



|                                                                                                  |                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | 建立要搭配執行緒抽取使用的資料處理器。 此 API 類似于 D3DX10CreateAsyncTextureInfoProcessor，但它也會載入紋理。 |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | 建立要搭配執行緒抽取使用的資料處理器。                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | 編譯著色器，並以非同步方式建立資料處理器。                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | 以非同步方式建立資料處理器的效果。                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | 以非同步方式建立效果集區。                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | 以非同步方式建立資料處理器。                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | 以非同步方式建立著色器的資料處理器。                                                                                               |



 

採用執行緒抽取作為參數的 Api。



|                                                                                                  |                                                                  |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | 從檔案編譯著色器。                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | 編譯位於記憶體中的著色器。                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | 從資源編譯著色器。                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | 從檔案建立效果。                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | 從記憶體建立效果。                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | 從資源建立效果。                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | 從檔案建立效果集區。                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | 從位於記憶體中的檔案建立效果集區。            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | 從資源建立效果集區。                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | 在不編譯的情況下，從檔案建立著色器。                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | 在不編譯的情況下，從記憶體建立著色器。                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | 從資源建立著色器，而不進行編譯。            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | 從檔案建立著色器資源檢視。                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | 從記憶體中的檔案建立著色器資源檢視。             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | 從資源建立著色器資源檢視。                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | 抓取指定影像檔案的相關資訊。                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | 取得已載入記憶體之映射的相關資訊。       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | 抓取資源中指定影像的相關資訊。         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | 從檔案建立材質資源。                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | 從位於系統記憶體中的檔案建立材質資源。 |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | 從其他資源建立材質資源。                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
