---
title: IMsTscAxEvents OnAuthenticationWarningDismissed 方法
description: 在 ActiveX 控制項顯示驗證對話方塊之後呼叫 (例如，[憑證錯誤] 對話方塊) 。
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- OnAuthenticationWarningDismissed 方法遠端桌面服務
- OnAuthenticationWarningDismissed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAuthenticationWarningDismissed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a55af8450160e271e96c53d4d5a9d4390393ab7880d2c2bb143cf0e6a1cb3bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125228"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>IMsTscAxEvents：： OnAuthenticationWarningDismissed 方法

在 ActiveX 控制項顯示驗證對話方塊之後呼叫 (例如，[憑證錯誤] 對話方塊) 。

## <a name="syntax"></a>語法


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如有需要，您可以使用 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)介面的 [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)屬性來還原可能已在 [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)方法中完成的任何父代。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windowsserver 2008、Windows server 2008 SP1<br/>                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





