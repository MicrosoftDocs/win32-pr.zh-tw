---
title: IMsTscAxEvents OnAuthenticationWarningDisplayed 方法
description: 在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，) [憑證錯誤] 對話方塊。
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
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094476"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>IMsTscAxEvents：： OnAuthenticationWarningDisplayed 方法

在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，) [憑證錯誤] 對話方塊。

## <a name="syntax"></a>語法


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如有需要，您可以使用 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)介面的 [ [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) ] 屬性，以確保顯示的 [強制回應驗證] 對話方塊會以指定的視窗作為父系 (這可能是在 [驗證] 對話方塊顯示) 時，防止使用者使用其他對話方塊的必要動作。 根據預設，父系是 ActiveX 控制項視窗。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008、Windows Server 2008 SP1<br/>                           |
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

 

 





