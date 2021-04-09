---
title: IDXCoreAdapterList::GetAdapter
description: 從 DXCore 介面卡清單物件的索引抓取特定的介面卡。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023903"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>IDXCoreAdapterList：： GetAdapter 方法

從 DXCore 介面卡清單物件的索引抓取特定的介面卡。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>參數

### <a name="index"></a>索引

類型： **uint32_t**

以零為基底的索引，識別 DXCore 介面卡清單中的介面卡實例。

### <a name="riid"></a>riid

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
|DXGI_ERROR_DEVICE_REMOVED|*索引* 是有效的，但介面卡不再處於有效的狀態。|
|E_INVALIDARG|提供的 *索引* 無效。|
|E_NOINTERFACE|針對 *riid* 提供的值無效。|
|E_POINTER|`nullptr` 是為 *ppvAdapter* 所提供。|

## <a name="remarks"></a>備註

傳遞代表相同介面卡之索引的多個呼叫會傳回相同的介面指標，甚至是跨不同的介面卡清單。 因此，可以安全地比較介面指標，以判斷多個指標是否參考相同的介面卡物件。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)