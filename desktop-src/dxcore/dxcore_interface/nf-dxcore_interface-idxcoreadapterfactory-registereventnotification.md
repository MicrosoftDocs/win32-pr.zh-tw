---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: 註冊以接收 DXCore 介面卡或介面卡清單中特定條件的通知。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b97b51f7c4359526317647b62241e37063243a56f45014c28ba2f2cd897706ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042896"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>IDXCoreAdapterFactory：： RegisterEventNotification 方法

註冊以接收 DXCore 介面卡或介面卡清單中特定條件的通知。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE RegisterEventNotification(
  _In_ IUnknown *dxCoreObject,
  DXCoreNotificationType notificationType,
  _In_ PFN_DXCORE_NOTIFICATION_CALLBACK callbackFunction,
  _In_opt_ void *callbackContext,
  _Out_ uint32_t *eventCookie) = 0;
```

## <a name="parameters"></a>參數

### <a name="dxcoreobject-in"></a>dxCoreObject [in]

類型： **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

DXCore 物件 ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 或 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)) 您要訂閱的通知。

### <a name="notificationtype"></a>notificationType

類型： **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

您要註冊的通知類型。 請參閱 [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) 中的表格，以取得哪些類型適用于哪些類型的物件的相關資訊。

### <a name="callbackfunction-in"></a>callbackFunction [in]

類型： **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

回呼函式的指標， (由您的應用程式所執行) ，由 DXCore 物件針對通知事件呼叫。 如需函數的簽章，請參閱 [PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)。

### <a name="callbackcontext-in"></a>callbackCoNtext [in]

類型： **void \***

包含內容資訊之物件的選擇性指標。 當通知引發時，這個物件會傳遞給您的回呼函數。

### <a name="eventcookie-out"></a>eventCookie [out]

類型： **uint32_t \***

**Uint32_t** 值的指標。 如果成功，函式會將指標取值，並將值設定為代表此註冊的非零 cookie 值。 您可以使用此 cookie 值，藉由呼叫 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)從通知取消註冊。 請參閱 **備註**。

如果不成功，則函式會將指標取值，並將值設為零，表示不正確 cookie 值。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|DXGI_ERROR_INVALID_CALL| (OS) 的作業系統不支援 *notificationType* 。|
|E_INVALIDARG|`nullptr` 提供給 *dxCoreObject*，或如果提供的 *notificationType* 和 *dxCoreObject* 組合無效，則為。|
|E_POINTER|`nullptr` 是針對 *callbackFunction* 或 *eventCookie* 所提供。|

## <a name="remarks"></a>備註

您可以使用 **RegisterEventNotification** 來註冊 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 和 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 介面所引發的事件。 支援這些通知類型。

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|支援的 *dxCoreObject*|備註|
|-|-|-|
|AdapterListStale|**IDXCoreAdapterList**|指出符合篩選準則的介面卡清單已變更。 如果介面卡清單在註冊時已過時，則會立即呼叫您的回呼。 每次註冊最多會發生一次此回呼。|
|AdapterNoLongerValid|**IDXCoreAdapter**|指出介面卡已不再有效。 如果介面卡在註冊時無效，則會立即呼叫您的回呼。|
|AdapterBudgetChange|**IDXCoreAdapter**|表示已發生記憶體預算事件，而且您應該使用[DXCoreAdapterState：：) AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)呼叫[IDXCoreAdapter：： QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (，以評估目前的記憶體預算狀態。 註冊時，一律會發生初始回呼，讓您查詢初始狀態。|
|AdapterHardwareContentProtectionTeardown|**IDXCoreAdapter**|指出您應該重新評估目前的加密會話狀態;例如，藉由呼叫 [ID3D11VideoCoNtext1：： CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) 來判斷特定 [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) 介面之硬體清除的影響。 註冊時，一律會發生初始回呼，讓您查詢初始狀態。|

呼叫您在 *callbackFunction* 中提供的函式，會在偵測到的事件發生時，透過 DXCore 在背景執行緒上以非同步方式進行。 不保證回呼的順序或時間有 &mdash; 多個回呼可能會以任何順序發生，甚至是同時進行。 在 **RegisterEventNotification** 完成之前，您的回呼甚至可能會叫用。 在此情況下，DXCore 會保證您的 *eventCookie* 會在呼叫回呼之前設定。 特定註冊的多個回呼將依序序列化。

回呼可能會在您呼叫 [UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)時隨時發生，而且會完成。 回呼會在自己的執行緒上執行，而且您可以在這些執行緒（包括 **UnregisterEventNotification**）上呼叫 DXCore API。 不過，您不能在這個執行緒上釋放 *dxCoreObject* 的最後一個參考。

> [!IMPORTANT]
> 在您終結傳遞給 **RegisterEventNotification** 的 *dxCoreObject* 引數所代表的 DXCore 物件之前，您必須使用 cookie 值，藉由呼叫 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)，從通知取消註冊該物件。 如果您沒有這麼做，則在偵測到情況時，就會引發嚴重的例外狀況。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)