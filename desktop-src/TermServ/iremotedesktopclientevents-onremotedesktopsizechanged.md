---
title: IRemoteDesktopClientEvents OnRemoteDesktopSizeChanged 方法
description: 當遠端桌面大小變更時呼叫。
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- OnRemoteDesktopSizeChanged 方法遠端桌面服務
- OnRemoteDesktopSizeChanged 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnRemoteDesktopSizeChanged 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685862"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a>IRemoteDesktopClientEvents：： OnRemoteDesktopSizeChanged 方法

當遠端桌面大小變更時呼叫。

## <a name="syntax"></a>語法


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*寬度* \[在\]
</dt> <dd></dd> <dt>

*高度* \[在\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                           |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                 |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





