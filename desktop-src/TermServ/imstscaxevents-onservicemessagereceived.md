---
title: IMsTscAxEvents OnServiceMessageReceived 方法
description: 當用戶端收到系統訊息時呼叫。
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- OnServiceMessageReceived 方法遠端桌面服務
- OnServiceMessageReceived 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnServiceMessageReceived 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686055"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a>IMsTscAxEvents：： OnServiceMessageReceived 方法

當用戶端收到系統訊息時呼叫。

## <a name="syntax"></a>語法


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*serviceMessage* \[在\]
</dt> <dd>

指定系統訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如需系統訊息的詳細資訊，請參閱 [設定遠端桌面閘道伺服器的訊息](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

