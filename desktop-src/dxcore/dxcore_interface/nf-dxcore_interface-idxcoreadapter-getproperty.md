---
title: IDXCoreAdapter::GetProperty
description: 抓取指定之介面卡屬性的值。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8adb48994580125d153c36394c4db65cb38f4a08306814d1638e5c27eb3d4868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279398"
---
# <a name="idxcoreadaptergetproperty-method"></a>IDXCoreAdapter：： GetProperty 方法

抓取指定之介面卡屬性的值。 在呼叫屬性類型的 **GetProperty** 之前，請先呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) ，確認此介面卡與作業系統 (OS) 可使用此屬性類型。 此外，在呼叫 **GetProperty** 之前，請先呼叫 [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) ，以判斷接收屬性值所需的緩衝區大小。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a>參數

### <a name="property"></a>屬性

類型： **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

您要取得其值之屬性的類型。 如需每個介面卡屬性的詳細資訊，請參閱 [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) 中的表格。

### <a name="buffersize"></a>bufferSize

類型： **size_t**

您在 *propertyData* 中配置並提供之輸出緩衝區的大小（以位元組為單位）。

### <a name="propertydata-out"></a>propertyData [out]

類型： **void \***

您在應用程式中配置的輸出緩衝區指標，且該函式會填入。 呼叫 [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) 來判斷 *propertyData* 緩衝區應針對指定介面卡屬性的大小。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|DXGI_ERROR_INVALID_CALL|此作業系統 (OS) 無法辨識 *屬性* 中指定的屬性類型。 呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) 確認此介面卡與作業系統 (OS) 可使用此屬性類型。|
|DXGI_ERROR_UNSUPPORTED|介面卡不支援 *屬性* 中指定的屬性類型。 呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) 確認此介面卡與作業系統 (OS) 可使用此屬性類型。|
|E_INVALIDARG|*PropertyData* 中提供的緩衝區大小不足。 呼叫 [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) 來判斷 *propertyData* 緩衝區應針對指定介面卡屬性的大小。|
|E_POINTER|`nullptr` 是為 *propertyData* 所提供。|

## <a name="remarks"></a>備註

您可以在不再有效的介面卡上呼叫 **GetProperty** ， &mdash; 因為這樣會導致該函式無法運作。 在填入之前，此函式會將 *propertyData* 緩衝區設為零。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)