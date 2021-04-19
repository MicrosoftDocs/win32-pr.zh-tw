---
description: 管理延遲的應用程式暫停作業。
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: 'ISuspendingDeferral 介面 (Windows. ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972857"
---
# <a name="isuspendingdeferral-interface"></a>ISuspendingDeferral 介面

管理延遲的應用程式暫停作業。

## <a name="members"></a>成員

**ISuspendingDeferral** 介面繼承自 [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)。 **ISuspendingDeferral** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISuspendingDeferral** 介面具有這些方法。



| 方法                                           | 描述                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**完成**](isuspendingdeferral-complete.md) | 通知系統應用程式已儲存其資料，並已準備好暫停。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>ApplicationModel。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ApplicationModel .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 
