---
title: IMsRdpClientNonScriptable NotifyRedirectDeviceChange 方法
description: 通知遠端桌面的裝置重新導向模組，ActiveX 控制系統上的裝置變更已發生。 這個方法會 \_ 將 WM DEVICECHANGE 通知傳遞給控制項。
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- NotifyRedirectDeviceChange 方法遠端桌面服務
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37986a218f672f5ace6d81b6496b958547e70a95f8ddea91bf6a130eb05b1ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130075"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>IMsRdpClientNonScriptable：： NotifyRedirectDeviceChange 方法

通知遠端桌面的裝置重新導向模組，ActiveX 控制系統上的裝置變更已發生。 這個方法會將 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 通知傳遞給控制項。

## <a name="syntax"></a>語法


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

指定裝置事件。 此參數可以是下列其中一個值。

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**


</dt> <dd>

已取消變更目前設定 (dock 或取消停駐) 的要求。

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ CONFIGCHANGED**


</dt> <dd>

目前的設定因 dock 或取消停駐而變更。

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**


</dt> <dd>

發生自訂事件。

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**


</dt> <dd>

已插入裝置，而且現在已可供使用。

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**


</dt> <dd>

要求許可權以移除裝置。 任何應用程式都可以拒絕此要求，並取消移除。

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**


</dt> <dd>

移除裝置的要求已取消。

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**


</dt> <dd>

裝置已移除。

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**


</dt> <dd>

即將移除裝置。 無法拒絕移除。

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**


</dt> <dd>

發生裝置特定事件。

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ 已變更**


</dt> <dd>

已在系統中新增或移除裝置。

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**


</dt> <dd>

已要求許可權來變更目前的設定 (dock 或移除) 。

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT 的 \_ 使用者**


</dt> <dd>

此訊息的意義是使用者定義的。

</dd> </dl> </dd> <dt>

*lParam* \[在\]
</dt> <dd>

包含事件特定資料之結構的指標。 其格式取決於 *wParam* 參數的值。 如需詳細資訊，請參閱每個事件的檔。 如需詳細資訊，請參閱 [裝置事件種類](/windows/desktop/DevIO/device-event-types)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

允許動態新增或移除裝置的容器應用程式，應該在其最上層視窗中處理 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 訊息，並使用 **NotifyRedirectDeviceChange** 方法將訊息轉送至控制項。 動態裝置變更的範例是當系統正在執行時，新增或移除重新導向的磁片磁碟機。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                     |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                               |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable 定義為2f079c4c-87b2-4afd-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

