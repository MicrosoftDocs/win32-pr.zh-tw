---
description: 表示非同步動作完成時所呼叫的方法。
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: AsyncActionCompletedHandler 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973466"
---
# <a name="asyncactioncompletedhandler-interface"></a>AsyncActionCompletedHandler 介面

表示非同步動作完成時所呼叫的方法。

## <a name="members"></a>成員

**AsyncActionCompletedHandler** 介面繼承自 [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)。 **AsyncActionCompletedHandler** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**AsyncActionCompletedHandler** 介面具有這些方法。



| 方法                                               | 描述                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**調用**](asyncactioncompletedhandler-invoke.md) | 叫用指定的非同步動作完成時所呼叫的方法。<br/> |



 

## <a name="remarks"></a>備註

將 **AsyncActionCompletedHandler** 指派給 [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) ，以在非同步動作完成時收到通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                    |
| 標頭<br/>                   | <dl> <dt>Windows .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

