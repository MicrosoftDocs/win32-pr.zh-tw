---
description: 註冊 Windows 映像取得 (WIA) 2.0 事件通知的執行中應用程式。
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'IWiaDevMgr2：： RegisterEventCallbackInterface 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192793"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>IWiaDevMgr2：： RegisterEventCallbackInterface 方法

註冊 Windows 映像取得 (WIA) 2.0 事件通知的執行中應用程式。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

指定 WIA 2.0 裝置的唯一識別碼。 將此參數設定為 **Null** ，以在所有 WIA 2.0 裝置上註冊事件。

</dd> <dt>

*pEventGUID* \[在\]
</dt> <dd>

類型： **CONST GUID \** _

指定應用程式所註冊之事件識別碼的指標。 請參閱標準事件識別碼的 [WIA 事件識別碼](-wia-wia-event-identifiers.md) 。

</dd> <dt>

_pIWiaEventCallback * \[ in\]
</dt> <dd>

類型： **[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _

指定 WIA 2.0 用來傳送事件通知之 [_ *IWiaEventCallback* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)介面的指標。

</dd> <dt>

*pEventObject* \[擴展\]
</dt> <dd>

類型： **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

接收 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

傳回標準 COM 錯誤碼或下列。



| 傳回碼                                                                               | Description                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl> | 無法傳回 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。 <br/> |



 

## <a name="remarks"></a>備註

> [!WARNING]
> 在仍映射服務重新開機後，使用相同進程中的 [**IWiaDevMgr：： RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface)、 **IWiaDevMgr2：： RegisterEventCallbackInterface** 和 [**DeviceManager**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) 方法，可能會導致存取違規，如果在服務停止之前使用了函數。

 

當 WIA 2.0 應用程式開始執行時，會使用這個方法來註冊以接收硬體裝置事件。 這可防止應用程式在另一個已註冊的事件發生時重新開機。 當應用程式呼叫 **IWiaDevMgr2：： RegisterEventCallbackInterface** 來註冊本身以接收來自裝置的 WIA 2.0 事件時，WIA 2.0 會將已註冊的事件路由至程式。

應用程式必須在透過 *pEventObject* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

> [!Note]  
> 在多執行緒應用程式中，事件通知回呼可能會與註冊回呼的執行緒位於不同的執行緒上。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
