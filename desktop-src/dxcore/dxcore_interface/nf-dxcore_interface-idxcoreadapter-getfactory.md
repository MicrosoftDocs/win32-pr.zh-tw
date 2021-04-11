---
title: IDXCoreAdapter::GetFactory
description: 抓取 DXCore 介面卡 factory 物件的 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) 介面指標。 |IDXCoreAdapter::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 1ac3e7fccd39b9b03ecb7016494a610519d26afa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196016"
---
# <a name="idxcoreadaptergetfactory-method"></a>IDXCoreAdapter：： GetFactory 方法

抓取 DXCore 介面卡 factory 物件的 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) 介面指標。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>參數

### <a name="riid"></a>riid

類型： **REFIID**

全域唯一識別碼的參考， (您想要在 *ppvFactory* 中傳回之介面的 GUID) 。 這應該是 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)的介面識別碼 (IID) 。

### <a name="ppvfactory-out"></a>ppvFactory [out]

類型： **void \* \***

具有在 *riid* 參數中指定之 IID 之介面指標的位址。 在成功傳回時， *\* ppvFactory* (已取值的位址) 包含現有 DXCore 介面卡 factory 物件的指標。 在傳回之前，函式會遞增 factory 物件之 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) 介面上的參考計數。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|E_NOINTERFACE|針對 *riid* 提供的值無效。|
|E_POINTER|`nullptr` 是為 *ppvFactory* 所提供。|

## <a name="remarks"></a>備註

在 [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) 介面、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 介面或 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 介面上存在參考的時間內，對 [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md)、 [IDXCoreAdapterList：： GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)或 [IDXCoreAdapter：： GetFactory]() 的其他呼叫會傳回相同物件的指標，並增加 **IDXCoreAdapterFactory** 介面的參考計數。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)
