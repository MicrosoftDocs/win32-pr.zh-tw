---
title: IMsTscAxEvents OnRequestGoFullScreen 方法
description: 當用戶端要求切換至全螢幕模式並呼叫 IMsTscAdvancedSettings put \_ ContainerHandledFullScreen 方法以將 ContainerHandledFullScreen 屬性設定為非零值時呼叫。
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- OnRequestGoFullScreen 方法遠端桌面服務
- OnRequestGoFullScreen 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRequestGoFullScreen 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6d689469f635694357890c620866fff5783680f8e9e8d11a1a05c78f6e1e322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770678"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a>IMsTscAxEvents：： OnRequestGoFullScreen 方法

當用戶端要求切換至全螢幕模式並呼叫 [**IMsTscAdvancedSettings：:p 使用 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 方法時呼叫，以將 **ContainerHandledFullScreen** 屬性設定為非零值。

## <a name="syntax"></a>語法


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在容器處理的全螢幕模式中，容器應進入標準全螢幕模式，以回應此事件。

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

 

 





