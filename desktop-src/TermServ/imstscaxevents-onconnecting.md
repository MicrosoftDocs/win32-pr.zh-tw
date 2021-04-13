---
title: IMsTscAxEvents OnConnecting 方法
description: 當用戶端控制項開始連接到伺服器以回應 IMsTscAx Connect 的呼叫時呼叫。
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- OnConnecting 方法遠端桌面服務
- OnConnecting 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnConnecting 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383874"
---
# <a name="imstscaxeventsonconnecting-method"></a>IMsTscAxEvents：： OnConnecting 方法

當用戶端控制項開始連接到伺服器以回應 [**IMsTscAx：： Connect**](imstscax-connect.md)的呼叫時呼叫。

## <a name="syntax"></a>語法


```C++
void OnConnecting();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在事件接收中執行此方法，以接收控制項已開始連接的通知。

## <a name="examples"></a>範例

下列範例示範如何使用 Visual Basic 腳本處理常式代碼來處理這個事件。 此範例中的假設是您的控制項物件名稱為 "MsRdpClient"。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



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

 

 





