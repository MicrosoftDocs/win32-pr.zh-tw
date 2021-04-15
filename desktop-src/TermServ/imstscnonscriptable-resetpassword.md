---
title: IMsTscNonScriptable ResetPassword 方法
description: 重設遠端桌面 ActiveX 控制項中的所有密碼狀態。
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- ResetPassword 方法遠端桌面服務
- ResetPassword 方法遠端桌面服務，IMsTscNonScriptable 介面
- IMsTscNonScriptable 介面遠端桌面服務，ResetPassword 方法
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466752"
---
# <a name="imstscnonscriptableresetpassword-method"></a>IMsTscNonScriptable：： ResetPassword 方法

重設遠端桌面 ActiveX 控制項中的所有密碼狀態。 您可以呼叫這個方法，以清除以下列三種支援格式之一儲存的密碼：純文字、可攜的編碼或二進位 (nonportable) 編碼。 請注意，編碼的密碼不應被安全地加密。

## <a name="syntax"></a>語法


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

您可以呼叫這個方法，在中斷連接之後重設控制項的密碼。 這樣可確保使用相同控制項實例的後續連接不會自動以先前設定的密碼登入。

只有當遠端桌面 ActiveX 控制項不是處於線上狀態時，您才能呼叫此方法。 如果在連接控制項時呼叫，這個方法 **會傳回 E \_ FAIL** 。 若要檢查連接狀態，請透過 [**IMsTscAx**](imstscax-interface.md)介面或繼承自它的其中一個介面，呼叫 [**get \_ connected**](imstscax-connected.md)方法。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable 定義為 c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





