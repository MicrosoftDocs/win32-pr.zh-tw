---
title: IDXCoreAdapter::GetPropertySize
description: 針對指定的介面卡屬性，會抓取 [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)呼叫所需的緩衝區大小（以位元組為單位）。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 525e2657ab7af5fa6f7cee4f527b74604d2674dbc67da232dd6501ddc45b0291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279250"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>IDXCoreAdapter：： GetPropertySize 方法

針對指定的介面卡屬性，會抓取 [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)呼叫所需的緩衝區大小（以位元組為單位）。 在呼叫屬性類型的 **GetPropertySize** 之前，請先呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) ，確認此介面卡與作業系統 (OS) 可使用此屬性類型。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>參數

### <a name="property"></a>屬性

類型： **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

您要取得其大小（以位元組為單位）的屬性類型。

### <a name="buffersize-out"></a>bufferSize [out]

類型： **size_t \***

**Size_t** 值的指標。 函式會對指標進行取值，並將值設定為輸出緩衝區的大小（以位元組為單位），您應該在呼叫 [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)時，將其配置並傳遞為 *propertyData* 引數。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|DXGI_ERROR_INVALID_CALL|此作業系統 (OS) 無法辨識 *屬性* 中指定的屬性類型。 呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) 確認此介面卡與作業系統 (OS) 可使用此屬性類型。|
|DXGI_ERROR_UNSUPPORTED|介面卡不支援 *屬性* 中指定的屬性類型。 呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) 確認此介面卡與作業系統 (OS) 可使用此屬性類型。|
|E_POINTER|`nullptr` 是針對 *bufferSize* 提供的。|

## <a name="remarks"></a>備註

您可以在不再有效的介面卡上呼叫 **GetPropertySize** ，函式 &mdash; 將不會失敗。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)