---
description: 任何自訂的影片篩選器篩選器都必須支援 IResize 介面，DirectShow 編輯服務 (DES) 。 若要設定自訂的調整器篩選，請在轉譯引擎上呼叫 IRenderEngine2：： SetResizerGUID 方法。
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: 'IResize 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 19aabd7c04cb5350ef3da87e1a20db6b75f6546f0fbcf5af3422c152bcafcf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818067"
---
# <a name="iresize-interface"></a>IResize 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IResize`任何自訂的影片篩選器篩選器都必須支援介面，DirectShow 編輯服務 (DES) 。 若要設定自訂的調整器篩選，請在轉譯引擎上呼叫 [**IRenderEngine2：： SetResizerGUID**](irenderengine2-setresizerguid.md) 方法。

## <a name="members"></a>成員

**IResize** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IResize** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IResize** 介面具有這些方法。



| 方法                                          | 描述                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**取得 \_ InputSize**](iresize-get-inputsize.md) | 傳回檔整器篩選的目前輸入大小。<br/>  |
| [**取得 \_ 媒體媒體**](iresize-get-mediatype.md) | 傳回檔整器篩選的輸出媒體類型。<br/>   |
| [**取得 \_ 大小**](iresize-get-size.md)           | 傳回目前的輸出大小和延展模式。<br/> |
| [**put \_ 媒體存放**](iresize-put-mediatype.md) | 設定輸出媒體類型。<br/>                       |
| [**放置 \_ 大小**](iresize-put-size.md)           | 設定輸出大小和延展模式。<br/>            |



 

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

 

 
