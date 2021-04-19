---
description: WPD 作業 \_ 會 \_ 指出列舉值會描述正在進行之作業的目前狀態。
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: 'WPD_OPERATION_STATES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984349"
---
# <a name="wpd_operation_states-enumeration"></a>WPD \_ 操作 \_ 狀態列舉

**WPD 作業 \_ 會 \_ 指出** 列舉值會描述正在進行之作業的目前狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**\_未指定 WPD 作業 \_ 狀態 \_**
</dt> <dd>

目前的作業處於未指定的狀態 (未設定) 和未知。

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD \_ 操作 \_ 狀態 \_ 已啟動**
</dt> <dd>

作業已啟動。

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD \_ 作業 \_ 狀態 \_ 正在執行**
</dt> <dd>

作業正在執行。

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD \_ 操作 \_ 狀態已 \_ 暫停**
</dt> <dd>

作業已暫停。

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD \_ 操作 \_ 狀態已 \_ 取消**
</dt> <dd>

作業已取消。

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD \_ 操作 \_ 狀態 \_ 已完成**
</dt> <dd>

作業已完成。

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD \_ 操作 \_ 狀態已 \_ 中止**
</dt> <dd>

作業已中止。

</dd> </dl>

## <a name="remarks"></a>備註

這些值會在應用程式定義的回呼中收到 ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




