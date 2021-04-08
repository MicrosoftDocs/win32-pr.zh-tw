---
title: IMsTscAxEvents OnRequestLeaveFullScreen 方法
description: 當用戶端要求離開全螢幕模式，且 IMsTscAdvancedSettings put \_ ContainerHandledFullScreen 屬性已設定為非零值時呼叫。
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- OnRequestLeaveFullScreen 方法遠端桌面服務
- OnRequestLeaveFullScreen 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRequestLeaveFullScreen 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686056"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a>IMsTscAxEvents：： OnRequestLeaveFullScreen 方法

當用戶端要求離開全螢幕模式，且 [**IMsTscAdvancedSettings：:p 的 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 屬性已設定為非零值時呼叫。

## <a name="syntax"></a>語法


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在容器處理的全螢幕模式中，容器應離開標準全螢幕模式，以回應此事件。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





