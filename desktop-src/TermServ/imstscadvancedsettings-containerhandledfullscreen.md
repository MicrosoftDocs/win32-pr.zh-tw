---
title: IMsTscAdvancedSettings ContainerHandledFullScreen 屬性
description: 指定是否啟用容器處理的全螢幕模式。
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- ContainerHandledFullScreen 屬性遠端桌面服務
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ContainerHandledFullScreen 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384889"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a>IMsTscAdvancedSettings：： ContainerHandledFullScreen 屬性

指定是否啟用容器處理的全螢幕模式。

> [!Note]  
> 當遠端桌面 ActiveX 控制項可以安全地進行腳本處理時， **ContainerHandledFullScreen** 屬性的值不會有任何作用，並且會在嘗試變更值時傳回 **S \_ FALSE** 。

 

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a>屬性值

將此參數設定為 **TRUE** ，以啟用模式或其他值以停用模式。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。 如果不支援，則傳回 **\_ FALSE** 。

## <a name="remarks"></a>備註

當啟用此模式時，目前的容器會將開關處理成全螢幕模式。 只有當目前的容器需要對全螢幕模式行為進行廣泛的控制時，才應該使用這個方法。 設定這個屬性時，控制項不會進入或離開全螢幕模式，以回應全螢幕模式快速鍵組合 (CTRL + ALT + BREAK) ;相反地，會呼叫 [**IMsTscAxEvents：： OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) 和 [**IMsTscAxEvents：： OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) 事件。 如需這些事件的詳細資訊，請參閱 [**IMsTscAxEvents**](imstscaxevents-interface.md) 。

大部分的容器應用程式都不需要使用容器處理的全螢幕模式。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





