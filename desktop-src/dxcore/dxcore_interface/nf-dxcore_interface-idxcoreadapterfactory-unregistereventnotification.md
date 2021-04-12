---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: 從您先前註冊的通知中取消註冊。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376297"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>IDXCoreAdapterFactory：： UnregisterEventNotification 方法

從您先前註冊的通知中取消註冊。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>參數

### <a name="eventcookie"></a>eventCookie

類型： **uint32_t**

當您呼叫 [IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) 代表您現在想要取消註冊的先前註冊時，會傳回 cookie 值 (傳回。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|E_INVALIDARG|*EventCookie* 的值不是代表先前註冊的有效 cookie。|

## <a name="remarks"></a>備註

只有在此註冊的所有擱置/進行中的回呼都已完成之後， **UnregisterEventNotification** 才會傳回。 DXCore 保證在 **UnregisterEventNotification** 傳回之後，不會對此註冊進行新的回呼。 不過，若要避免鎖死，如果您從回呼內呼叫 **UnregisterEventNotification** ， **UnregisterEventNotification** 就不會等待作用中的回呼完成。

> [!IMPORTANT]
> 在您終結傳遞給 [IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)之 *dxCoreObject* 引數所代表的 DXCore 物件之前，您必須使用 cookie 值，藉由呼叫 **UnregisterEventNotification** 從通知取消註冊該物件。 如果您沒有這麼做，則在偵測到情況時，就會引發嚴重的例外狀況。

當您取消註冊 cookie 值之後，該值就會符合後續註冊所傳回的資格

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)