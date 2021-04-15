---
title: IDXCoreAdapterFactory::CreateAdapterList
description: 產生介面卡物件的清單，表示系統目前的介面卡狀態，並符合指定的準則。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463460"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>IDXCoreAdapterFactory：： CreateAdapterList 方法

產生介面卡物件的清單，表示系統目前的介面卡狀態，並符合指定的準則。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a>參數

### <a name="numattributes"></a>numAttributes

類型： **uint32_t**

*FilterAttributes* 引數所指向之陣列中的元素數目。

### <a name="filterattributes-in"></a>filterAttributes [in]

類型： **CONST GUID \***

介面卡屬性 Guid 陣列的指標。 如需屬性 Guid 清單，請參閱 [DXCore adapter 屬性 guid](../dxcore-adapter-attribute-guids.md)。 至少必須提供一個 GUID。 在陣列中提供一個以上的 GUID 的情況下，傳回的清單中只會包含符合 *所有* 要求屬性的介面卡。

### <a name="riid"></a>riid

類型： **REFIID**

全域唯一識別碼的參考， (您想要在 *ppvAdapterList* 中傳回之介面的 GUID) 。 這應該是 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)的介面識別碼 (IID) 。

### <a name="ppvadapterlist-out"></a>ppvAdapterList [out]

類型： **void \* \***

具有在 *riid* 參數中指定之 IID 之介面指標的位址。 在成功傳回時， *\* ppvAdapterList* (已取值的位址) 包含已建立之介面卡清單的指標。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|E_INVALIDARG|`nullptr` 為 *filterAttributes* 提供，或為 *numAttributes* 提供0。|
|E_NOINTERFACE|針對 *riid* 提供的值無效。|
|E_POINTER|`nullptr` 是為 *ppvAdapterList* 所提供。|

## <a name="remarks"></a>備註

即使找不到介面卡，只要引數有效， **CreateAdapterList** 就會建立有效的 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件，並傳回 **S_OK**。 產生之後，此特定清單中的介面卡不會變更。 但是，如果其中一張介面卡變成無效，或新的介面卡抵達符合提供的篩選準則，則會將清單視為過時。 **CreateAdapterList** 傳回的清單不會以任何特定方式排序，但是清單的順序在多個呼叫之間是一致的，甚至是跨作業系統重新開機。 順序可能會在系統設定變更時變更，包括新增或移除介面卡，或在現有的介面卡上進行驅動程式更新。 您可以使用 [IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) 來註冊這些變更，其方式是使用通知類型 **DXCoreNotificationType. AdapterListStale**。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)