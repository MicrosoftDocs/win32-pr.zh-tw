---
title: IMsTscAxEvents OnLoginComplete 方法
description: 當用戶端控制項成功登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器時呼叫，並遵循 [Windows 登入] 對話方塊的顯示。
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- OnLoginComplete 方法遠端桌面服務
- OnLoginComplete 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnLoginComplete 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6c89b494a250652e054e245eb0de3267a860bec1a193c7dc953f93fd0800c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138431"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>IMsTscAxEvents：： OnLoginComplete 方法

當用戶端控制項成功登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器時呼叫，並遵循 [Windows 登入] 對話方塊的顯示。

## <a name="syntax"></a>語法


```C++
void OnLoginComplete();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在事件接收中執行此方法，以接收控制項已完成登入的通知。

## <a name="examples"></a>範例

下列範例示範如何使用 Visual Basic 腳本處理常式代碼來處理這個事件。 此範例中的假設是您的控制項物件名稱為 "MsRdpClient"。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
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

 

 





