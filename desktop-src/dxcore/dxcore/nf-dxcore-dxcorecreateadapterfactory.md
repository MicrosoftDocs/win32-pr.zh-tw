---
title: DXCoreCreateAdapterFactory
description: 建立可用來產生進一步 DXCore 物件的 DXCore 介面卡 factory。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 90567d732f6febc5d95b460b2ff88929dd12b2f22275de9db0d6bc5f88ef99ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985178"
---
# <a name="dxcorecreateadapterfactory-function"></a>DXCoreCreateAdapterFactory 函式

## <a name="description"></a>描述

建立可用來產生進一步 DXCore 物件的 DXCore 介面卡 factory。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="parameters"></a>參數

### <a name="riid"></a>riid

類型： **REFIID**

全域唯一識別碼的參考， (您想要在 *ppvFactory* 中傳回之介面的 GUID) 。 這應該是 [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md)的介面識別碼 (IID) 。

### <a name="ppvfactory-out"></a>ppvFactory [out]

類型： **void \* \***

具有在 *riid* 參數中指定之 IID 之介面指標的位址。 在成功傳回時， *\* ppvFactory* (已取值的位址) 包含已建立之 DXCore factory 的指標。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|E_NOINTERFACE|針對 *riid* 提供的值無效。|
|E_POINTER|`nullptr` 是為 *ppvFactory* 所提供。|

## <a name="remarks"></a>備註

在 [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) 介面、 [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) 介面或 [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) 介面上存在參考的時間內，對 **DXCoreCreateAdapterFactory**、 [IDXCoreAdapterList：： GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)或 [IDXCoreAdapter：： GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) 的其他呼叫會傳回相同物件的指標，並增加 **IDXCoreAdapterFactory** 介面的參考計數。

## <a name="see-also"></a>另請參閱

[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)