---
description: 提供應用程式暫停事件的資料。
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: 'ISuspendingEventArgs 介面 (Windows. ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970175"
---
# <a name="isuspendingeventargs-interface"></a>ISuspendingEventArgs 介面

提供應用程式暫停事件的資料。

## <a name="members"></a>成員

**ISuspendingEventArgs** 介面繼承自 [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)。 **ISuspendingEventArgs** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ISuspendingEventArgs** 介面具有這些屬性。



| 屬性                                                                           | 存取類型           | Description                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**SuspendingOperation**](isuspendingeventargs-suspendingoperation.md)<br/> | 讀取/寫入<br/> | 取得應用程式暫停作業。<br/> |



 

## <a name="remarks"></a>備註

當您執行事件處理常式（例如 [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041)、 [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)），並 [**新增 \_ 暫停**](/previous-versions//hh438376(v=vs.85)) 以回應應用程式暫止事件時，就會存取這個物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 標頭<br/>                   | <dl> <dt>ApplicationModel。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ApplicationModel .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 
