---
description: IAMSetErrorLog 介面會設定或抓取 DirectShow 編輯服務 (DES) 的錯誤記錄檔。
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: 'IAMSetErrorLog 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a16e56de7f350b30c1b92c0c94ff3e3e06afc31b363c0b3a6e98017ce483aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756398"
---
# <a name="iamseterrorlog-interface"></a>IAMSetErrorLog 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMSetErrorLog`介面會設定或抓取[DirectShow 編輯服務](directshow-editing-services.md) (DES) 的錯誤記錄檔。 時間軸物件會執行這個介面。 應用程式可以使用這個介面來記錄執行時間的轉譯錯誤。 在您的應用程式中執行 [**IAMErrorLog**](iamerrorlog.md) 介面，然後在時間軸上呼叫 [**IAMSetErrorLog：:p 的 \_ 錯誤**](iamseterrorlog-put-errorlog.md) 記錄檔方法。

如需使用此介面的詳細資訊，請參閱 [記錄錯誤](logging-errors.md)。

## <a name="members"></a>成員

**IAMSetErrorLog** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMSetErrorLog** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMSetErrorLog** 介面具有這些方法。



| 方法                                               | 描述                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**取得 \_ 錯誤記錄檔**](iamseterrorlog-get-errorlog.md) | 抓取這個物件目前的錯誤記錄檔。<br/> |
| [**put \_ 錯誤記錄檔**](iamseterrorlog-put-errorlog.md) | 指定物件的錯誤記錄檔。<br/>           |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
