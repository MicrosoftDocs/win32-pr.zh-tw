---
description: IWiaDevMgr2：： RegisterEventCallbackCLSID 方法會註冊應用程式以接收事件，即使應用程式並未執行也一樣。
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'IWiaDevMgr2：： RegisterEventCallbackCLSID 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9137fdd33f59eb841a54e84a6d12bb0b08968ac29c8737afbf56f66c57176c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965646"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>IWiaDevMgr2：： RegisterEventCallbackCLSID 方法

**IWiaDevMgr2：： RegisterEventCallbackCLSID** 方法會註冊應用程式以接收事件，即使應用程式並未執行也一樣。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

指定註冊旗標。 可以設定為下列值：



| 註冊旗標                | 意義                                           |
|----------------------------------|---------------------------------------------------|
| WIA \_ 註冊 \_ 事件 \_ 回呼   | 報名活動。                           |
| WIA \_ 取消註冊 \_ 事件 \_ 回呼 | 刪除事件的註冊。            |
| WIA \_ 設定 \_ 預設 \_ 處理常式       | 將應用程式設定為預設事件處理常式。 |



 

</dd> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

指定裝置識別碼。 傳遞 **Null** 以註冊所有 WIA 2.0 裝置上的事件。

</dd> <dt>

*pEventGUID* \[在\]
</dt> <dd>

類型： **CONST GUID \***

指定應用程式註冊的事件。 如需標準事件的清單，請參閱 [WIA 事件識別碼](-wia-wia-event-identifiers.md)。

</dd> <dt>

*pClsID* \[在\]
</dt> <dd>

類型： **CONST GUID \***

應用程式類別識別碼的指標 (**CLSID**) 。 當事件發生時，WIA 2.0 執行時間系統會使用應用程式 **CLSID** 來啟動應用程式。

</dd> <dt>

*bstrName* \[在\]
</dt> <dd>

類型： **BSTR**

指定為事件註冊的應用程式名稱。

</dd> <dt>

*bstrDescription* \[在\]
</dt> <dd>

類型： **BSTR**

指定針對事件註冊之應用程式的文字描述。

</dd> <dt>

*bstrIcon* \[在\]
</dt> <dd>

類型： **BSTR**

指定要用於註冊事件之應用程式圖示的影像檔案名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

WIA 2.0 應用程式會使用這個方法來註冊，以接收硬體裝置事件。 在呼叫 **IWiaDevMgr2：： RegisterEventCallbackCLSID** 之後，應用程式會註冊以接收 WIA 2.0 裝置事件，即使它並未執行也一樣。

當事件發生時，WIA 2.0 系統會決定要註冊哪個應用程式以接收事件。 它會使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數和 *pClsID* 參數中指定的 CLSID 來建立應用程式的實例，然後呼叫 [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) 方法，將事件資訊傳送至應用程式。

應用程式可以叫用 [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 方法來列舉事件註冊資訊。

如果應用程式不是已註冊的元件物件模型 (COM) 元件，而且與 WIA 2.0 架構不相容，請使用 [**IWiaDevMgr2：： RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) 方法來註冊裝置事件的應用程式。

> [!Note]  
> 在多執行緒應用程式中，並不保證會在註冊回呼的相同執行緒上傳回事件通知回呼。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl> |



 

 
