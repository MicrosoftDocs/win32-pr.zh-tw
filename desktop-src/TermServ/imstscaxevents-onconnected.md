---
title: IMsTscAxEvents OnConnected 方法
description: 當用戶端控制項正在建立與遠端桌面工作階段主機 (RD 工作階段主機) server 的連接時呼叫。
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- OnConnected 方法遠端桌面服務
- OnConnected 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnConnected 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685863"
---
# <a name="imstscaxeventsonconnected-method"></a>IMsTscAxEvents：： OnConnected 方法

當用戶端控制項正在建立與遠端桌面工作階段主機 (RD 工作階段主機) server 的連接時呼叫。

## <a name="syntax"></a>語法


```C++
void OnConnected();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在您的事件接收器中執行此方法，以接收控制項已建立與 RD 工作階段主機伺服器之連接的通知。

如需呼叫這個方法的詳細資訊，請參閱 [**IMsTscAxEvents：： OnLoginComplete**](imstscaxevents-onlogincomplete.md) 事件。

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

 

 





