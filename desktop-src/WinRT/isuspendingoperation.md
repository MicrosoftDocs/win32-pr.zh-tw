---
description: 提供應用程式暫停作業的相關資訊。
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: 'ISuspendingOperation 介面 (Windows. ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511476"
---
# <a name="isuspendingoperation-interface"></a>ISuspendingOperation 介面

提供應用程式暫停作業的相關資訊。

## <a name="members"></a>成員

**ISuspendingOperation** 介面繼承自 [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)。 **ISuspendingOperation** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ISuspendingOperation** 介面具有這些方法。



| 方法                                                  | 描述                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**GetDeferral**](isuspendingoperation-getdeferral.md) | 要求應用程式暫停操作延遲。<br/> |



 

### <a name="properties"></a>屬性

**ISuspendingOperation** 介面具有這些屬性。



| 屬性                                                     | 存取類型           | Description                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**期限**](isuspendingoperation-deadline.md)<br/> | 讀取/寫入<br/> | 取得延遲的應用程式暫停作業繼續之前剩餘的時間。<br/> |



 

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

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 
