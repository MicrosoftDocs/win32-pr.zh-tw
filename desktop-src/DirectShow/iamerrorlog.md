---
description: IAMErrorLog 介面提供在 DirectShow 編輯服務 (DES) 中進行錯誤記錄的回呼方法。DES 不會執行這個介面。
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: 'IAMErrorLog 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994652"
---
# <a name="iamerrorlog-interface"></a>IAMErrorLog 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMErrorLog`介面會在 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)中提供回呼方法，以進行錯誤記錄。

DES 不會執行這個介面。 若要執行錯誤記錄，請在您的應用程式中執行此介面，並在時間軸上呼叫 [**IAMSetErrorLog：:p \_ 錯誤**](iamseterrorlog-put-errorlog.md) 記錄檔。 如果轉譯專案時發生錯誤，DES 會呼叫您的應用程式所執行的 [**IAMErrorLog：： LogError**](iamerrorlog-logerror.md) 方法。

只有當您使用 [**IRenderEngine**](irenderengine.md) 介面呈現專案時，DES 才會記錄錯誤。 例如，如果您將專案儲存為 DirectShow 篩選圖形 ( grf 格式) 並播放圖形檔案，則不會記錄錯誤。 如需使用此介面的詳細資訊，請參閱 [記錄錯誤](logging-errors.md)。

## <a name="members"></a>成員

**IAMErrorLog** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMErrorLog** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMErrorLog** 介面具有這些方法。



| 方法                                   | 描述               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | 記錄錯誤。<br/> |



 

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



 

 
