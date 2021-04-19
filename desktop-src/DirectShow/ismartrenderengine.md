---
description: ISmartRenderEngine 介面提供的方法，可支援 DirectShow 編輯服務中的智慧型 recompression (DES) 。 智慧型轉譯引擎會公開這個介面。
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: 'ISmartRenderEngine 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999211"
---
# <a name="ismartrenderengine-interface"></a>ISmartRenderEngine 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`ISmartRenderEngine`介面提供的方法可支援[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中的智慧型 recompression。 智慧型轉譯引擎會公開這個介面。

## <a name="members"></a>成員

**ISmartRenderEngine** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ISmartRenderEngine** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISmartRenderEngine** 介面具有這些方法。



| 方法                                                                | 描述                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md)   | 抓取指定群組的壓縮篩選。<br/>                 |
| [**SetFindCompressorCB**](ismartrenderengine-setfindcompressorcb.md) | 未實作。<br/>                                                          |
| [**SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md)   | 指定轉譯指定群組時要使用的壓縮篩選。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[轉譯專案](rendering-a-project.md)
</dt> </dl>

 

 
