---
title: 'ID3DX11Effect 介面 (D3dx11effect .h) '
description: ID3DX11Effect 介面會管理一組用於執行轉譯效果的狀態物件、資源和著色器。
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- ID3DX11Effect 介面 Direct3D 11
- ID3DX11Effect 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4270059d02aec10905ea8aed7754bfb3a34c6897
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479144"
---
# <a name="id3dx11effect-interface"></a>ID3DX11Effect 介面

**ID3DX11Effect** 介面會管理一組用於執行轉譯效果的狀態物件、資源和著色器。

## <a name="members"></a>成員

**ID3DX11Effect** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX11Effect** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11Effect** 介面具有這些方法。



| 方法                                                                     | 描述                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | 建立效果介面的複本。<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | 取得類別連結介面。<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | 依索引取得常數緩衝區。<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | 依名稱取得常數緩衝區。<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | 取得效果描述。<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | 取得建立效果的裝置。<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | 依索引取得效果群組。<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | 依名稱取得效果群組。<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | 依索引取得技術。<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | 依名稱取得技術。<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | 依索引取得變數。<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | 依名稱取得變數。<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | 依語義取得變數。<br/>                                                    |
| [**IsOptimized**](id3dx11effect-isoptimized.md)                           | 測試效果，以查看反映中繼資料是否已從記憶體中移除。<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | 測試效果，以查看它是否包含有效的語法。<br/>                             |
| [**最佳化**](id3dx11effect-optimize.md)                                 | 將效果所需的記憶體數量降到最低。<br/>                          |



 

## <a name="remarks"></a>備註

藉由呼叫 [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)來建立效果。

效果系統會將轉譯所需的資訊群組為包含：用於指派群組中狀態變更的狀態物件、提供輸入資料和儲存輸出資料的資源，以及控制轉譯如何完成的程式，稱為著色器。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

> [!Note]
>
> 如果您呼叫 **ID3DX11Effect** 物件上的 [**Queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取出 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面， **queryinterface** 會傳回 E \_ NOINTERFACE。 若要解決此問題，請使用下列程式碼：
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;&gt;     pIUnknown-&gt;AddRef();</code></pre> | 

>
> 
>
>  

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------|-------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |

## <a name="see-also"></a>另請參閱

[效果11介面](d3d11-graphics-reference-effects11-interfaces.md)

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
