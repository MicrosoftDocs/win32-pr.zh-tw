---
title: IMsTscAxEvents OnRemoteWindowDisplayed 方法
description: 當 RemoteApp 視窗顯示時呼叫。
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- OnRemoteWindowDisplayed 方法遠端桌面服務
- OnRemoteWindowDisplayed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRemoteWindowDisplayed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6985a71fe6351a81b2daef69401dfd5c65543e9984fd64c28a120704a34d5a8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512108"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>IMsTscAxEvents：： OnRemoteWindowDisplayed 方法

當 RemoteApp 視窗顯示時呼叫。

## <a name="syntax"></a>語法


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*vbDisplayed* \[在\]
</dt> <dd>

Type： **VARIANT \_ BOOL**

指出是否要顯示或隱藏 RemoteApp 視窗。

</dd> <dt>

*hwnd* \[在\]
</dt> <dd>

類型： **HWND**

視窗的控制碼隨即顯示。

</dd> <dt>

*windowAttribute* \[在\]
</dt> <dd>

類型： **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)列舉的值，可指定事件的詳細資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





