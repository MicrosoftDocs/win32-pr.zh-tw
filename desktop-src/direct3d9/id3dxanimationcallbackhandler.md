---
description: 應用程式會在呼叫 ID3DXAnimationController：： AdvanceTime 所產生的動畫集中，執行此介面來處理回呼。
ms.assetid: 5a24ac96-2e68-49c0-acf6-8715d87b202d
title: 'ID3DXAnimationCallbackHandler 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb3b58c58c6a0bd71924fb207170a177797b9f84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992134"
---
# <a name="id3dxanimationcallbackhandler-interface"></a>ID3DXAnimationCallbackHandler 介面

應用程式會在呼叫 [**ID3DXAnimationController：： AdvanceTime**](id3dxanimationcontroller--advancetime.md)所產生的動畫集中，執行此介面來處理回呼。

## <a name="members"></a>成員

**ID3DXAnimationCallbackHandler** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXAnimationCallbackHandler** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXAnimationCallbackHandler** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HandleCallback**](id3dxanimationcallbackhandler--handlecallback.md) | 應用程式會執行此方法。 呼叫 [**ID3DXAnimationController：： AdvanceTime**](id3dxanimationcontroller--advancetime.md)期間，在其中一個追蹤中設定動畫的回呼時，會呼叫這個方法。<br/> |



 

## <a name="remarks"></a>備註

LPD3DXANIMATIONCALLBACKHANDLER 型別定義為這個介面的指標。


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
