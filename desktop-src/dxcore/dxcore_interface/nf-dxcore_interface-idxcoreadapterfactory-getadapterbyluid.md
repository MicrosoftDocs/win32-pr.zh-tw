---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: 取得指定之 LUID 的 DXCore 介面卡物件 ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) （如果有的話）。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d8f72aba23b9a1f57094b39e5afba3740f8749348c6a2da6a8753f72a7a0e6ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787049"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>IDXCoreAdapterFactory：： GetAdapterByLuid 方法

取得指定之 LUID 的 DXCore 介面卡物件 ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) （如果有的話）。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>參數

### <a name="adapterluid"></a>adapterLUID

類型： **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**

識別介面卡實例的本地唯一值。

### <a name="riid-in"></a>riid [in]

類型： **REFIID**

全域唯一識別碼的參考， (您想要在 *ppvAdapter* 中傳回之介面的 GUID) 。 這應該是 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)的介面識別碼 (IID) 。

### <a name="ppvadapter-out"></a>ppvAdapter [out]

類型： **void \* \***

具有在 *riid* 參數中指定之 IID 之介面指標的位址。 在成功傳回時， *\* ppvAdapter* (已取值的位址) 包含已建立之 DXCore 介面卡的指標。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|已辨識傳入 *adapterLUID* 的介面卡 LUID，但介面卡已不再處於有效狀態。|
|E_INVALIDARG|由於 *adapterLUID* 中傳遞的值可透過 DXCore 取得，因此不會有這種介面卡 LUID。|
|E_NOINTERFACE|針對 *riid* 提供的值無效。|
|E_POINTER|`nullptr` 是為 *ppvAdapter* 所提供。|

## <a name="remarks"></a>備註

傳遞相同 [LUID](/windows/win32/api/winnt/ns-winnt-luid) 的多個呼叫會傳回相同的介面指標。 因此，可以安全地比較介面指標，以判斷多個指標是否參考相同的介面卡物件。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)