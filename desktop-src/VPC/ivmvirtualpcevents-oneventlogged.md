---
title: 'IVMVirtualPCEvents OnEventLogged 方法 (VPCCOMInterfaces .h) '
description: 接收 Windows Virtual PC 記錄事件的通知。
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- OnEventLogged 方法 Virtual PC
- OnEventLogged 方法 Virtual PC，IVMVirtualPCEvents 介面
- IVMVirtualPCEvents 介面 Virtual PC，OnEventLogged 方法
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4994f37cd0e6f83162171fbbdacbf2247a8d472cd49b5750aa2d1b735e4b554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998518"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>IVMVirtualPCEvents：： OnEventLogged 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

接收 Windows Virtual PC 記錄事件的通知。

## <a name="syntax"></a>語法


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*logMessageID* \[在\]
</dt> <dd>

已記錄之事件記錄檔訊息的訊息識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當 Windows Virtual PC 將訊息記錄到 Windows 事件記錄檔時，就會呼叫這個方法。 用戶端程式必須執行這個介面方法，以接收來自 [**IVMVirtualPC**](ivmvirtualpc.md)的 **vmVirtualPCEvent \_ EventLogged** 事件的通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents 定義為 efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

