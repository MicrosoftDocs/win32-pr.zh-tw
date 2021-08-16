---
title: IMsTscAxEvents OnAuthenticationWarningDisplayed 方法
description: 在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，[憑證錯誤] 對話方塊) 。
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- OnAuthenticationWarningDisplayed 方法遠端桌面服務
- OnAuthenticationWarningDisplayed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAuthenticationWarningDisplayed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df2de56a612c748db720e485d9f1e6e5750c9fc3281500dfddd751f41aed1641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854006"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>IMsTscAxEvents：： OnAuthenticationWarningDisplayed 方法

在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，[憑證錯誤] 對話方塊) 。

## <a name="syntax"></a>語法


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如有需要，您可以使用 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)介面的 [ [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) ] 屬性，以確保顯示的 [強制回應驗證] 對話方塊會以指定的視窗作為父系 (這可能是在 [驗證] 對話方塊顯示) 時，防止使用者使用其他對話方塊的必要動作。 根據預設，父系是 ActiveX 控制視窗。

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

[**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





