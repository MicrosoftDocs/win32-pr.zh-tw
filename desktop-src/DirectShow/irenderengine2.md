---
description: IRenderEngine2 介面可讓應用程式取代 DirectShow 編輯服務 (DES) 所使用的預設影片調整大小篩選。 基本轉譯引擎和智慧型轉譯引擎都支援此介面。
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: 'IRenderEngine2 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 39f1bc68fc6cd76e87d1998047cb211b3a8aa8e263c90e0494c7eaf15d52f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818506"
---
# <a name="irenderengine2-interface"></a>IRenderEngine2 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IRenderEngine2`介面可讓應用程式取代 DirectShow 編輯服務 (DES) 所使用的預設影片調整大小篩選。 [基本轉譯引擎](basic-render-engine.md)和智慧型轉譯[引擎](smart-render-engine.md)都支援此介面。

## <a name="members"></a>成員

**IRenderEngine2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IRenderEngine2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IRenderEngine2** 介面具有這些方法。



| 方法                                                  | 描述                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | 指定應用程式所提供之自訂調整大小篩選的 CLSID。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | DirectX 9.0 或更新版本<br/>                                                         |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[提供自訂的影片調整](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
