---
description: ID3DXInclude 是使用者執行的介面，可為 \# 著色器編譯期間的 include 指示詞提供回呼。
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: 'ID3DXInclude 介面 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991494"
---
# <a name="id3dxinclude-interface"></a>ID3DXInclude 介面

ID3DXInclude 是使用者執行的介面，可為 \# 著色器編譯期間的 include 指示詞提供回呼。 這個介面中的每個方法都必須由使用者執行，當發生下列其中一種情況時，就會用來做為應用程式的回呼：

-   包含包含的 HLSL 著色器 \# 會藉由呼叫其中一個 D3DXCompileShader 函數來進行編譯 \* \* \* 。
-   元件著色器 \# 包含的組合是藉由呼叫任何 D3DXAssembleShader \* \* \* 函數。
-   包含包含的效果 \# 會藉由呼叫任何 D3DXCreateEffect \* \* \* 或 D3DXCreateEffectCompiler \* \* \* 函數來編譯。

## <a name="members"></a>成員

**ID3DXInclude** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXInclude** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXInclude** 介面具有這些方法。



| 方法                               | 描述                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**關閉**](id3dxinclude--close.md) | 使用者執行的方法，用於關閉著色器的 \# 包含檔案。<br/>                             |
| [**打開**](id3dxinclude--open.md)   | 使用者執行的方法，用來開啟和讀取著色器包含檔案的內容 \# 。<br/> |



 

## <a name="remarks"></a>備註

使用者藉由實作為衍生自這個介面的類別，以及執行所有介面方法，來建立 ID3DXInclude 介面。

LPD3DXINCLUDE 型別定義為這個介面的指標。


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果介面](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
