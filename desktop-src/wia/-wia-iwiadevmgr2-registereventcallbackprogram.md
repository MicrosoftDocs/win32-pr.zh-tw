---
description: IWiaDevMgr2：： RegisterEventCallbackProgram 方法會註冊應用程式以接收裝置事件。 它主要是為了提供與未針對 Windows 映像取得所撰寫之應用程式的回溯相容性， (WIA) 2.0。
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'IWiaDevMgr2：： RegisterEventCallbackProgram 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974084"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>IWiaDevMgr2：： RegisterEventCallbackProgram 方法

**IWiaDevMgr2：： RegisterEventCallbackProgram** 方法會註冊應用程式以接收裝置事件。 它主要是為了提供與未針對 Windows 映像取得所撰寫之應用程式的回溯相容性， (WIA) 2.0。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

註冊旗標。 可以設定為下列值。



| 值                                                                                                                                                                                                           | 意義                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**WIA \_ 註冊 \_ 事件 \_ 回呼**</dt> </dl>       | 報名活動。<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**WIA \_ 取消註冊 \_ 事件 \_ 回呼**</dt> </dl> | 刪除事件的註冊。<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**WIA \_ 設定 \_ 預設 \_ 處理常式**</dt> </dl>                   | 將應用程式設定為預設事件處理常式。<br/> |



 

</dd> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

裝置識別碼。 傳遞 **Null** 以註冊所有 WIA 2.0 裝置上的事件。

</dd> <dt>

*pEventGUID* \[在\]
</dt> <dd>

類型： **CONST GUID \** _

應用程式正在註冊的事件。 如需有效的事件 Guid 清單，請參閱 [WIA 事件識別碼](-wia-wia-event-identifiers.md)。

</dd> <dt>

_bstrFullAppName * \[ in\]
</dt> <dd>

類型： **BSTR**

應用程式的完整路徑名稱。

</dd> <dt>

*bstrCommandlineArg* \[在\]
</dt> <dd>

類型： **BSTR**

應用程式的適當命令列引數。

</dd> <dt>

*bstrName* \[在\]
</dt> <dd>

類型： **BSTR**

應用程式的名稱。 當有多個應用程式註冊相同的事件時，就會向使用者顯示名稱。

</dd> <dt>

*bstrDescription* \[在\]
</dt> <dd>

類型： **BSTR**

應用程式的描述。 當有多個應用程式註冊相同的事件時，就會向使用者顯示描述。

</dd> <dt>

*bstrIcon* \[在\]
</dt> <dd>

類型： **BSTR**

表示應用程式的圖示。 當有多個應用程式註冊相同的事件時，使用者會看到圖示。 字串包含應用程式的名稱，以及圖示以零為基底的索引（以逗號分隔），例如 "MyApp，0"。 可能有一個以上代表應用程式的圖示。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用 **IWiaDevMgr2：： RegisterEventCallbackProgram** 來註冊硬體裝置事件。 當應用程式註冊的事件發生時，就會啟動應用程式，並將事件資訊傳送至應用程式。

您可以使用 [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 方法來取得事件註冊屬性之列舉值物件的指標。

只使用 **IWiaDevMgr2：： RegisterEventCallbackProgram** 方法，與未針對 WIA 2.0 架構撰寫的應用程式回溯相容。 針對新的應用程式，使用 WIA 2.0 架構所提供的 COM) 介面 (元件物件模型。 具體而言，請呼叫 [**IWiaDevMgr2：： RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) 或 [**IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) ，以針對裝置事件註冊新的應用程式。

一般來說，這個方法是由安裝程式或腳本呼叫。 安裝程式或腳本會註冊應用程式，以接收 WIA 2.0 裝置事件。 當事件發生時，WIA 2.0 執行時間系統會啟動應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl> |



 

 




