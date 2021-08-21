---
title: IDXCoreAdapter::SetState
description: 在介面卡上設定指定專案的狀態。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c80ca670be26ffdcefa5e89cee079d2225d204ee97e99e41f69686300a46230b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042906"
---
# <a name="idxcoreadaptersetstate-method"></a>IDXCoreAdapter：： SetState 方法

在介面卡上設定指定專案的狀態。 在呼叫屬性類型的 **SetState** 之前，請先呼叫 [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) ，確認此介面卡和作業系統 (OS) 的設定狀態種類是否可用。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a>參數

### <a name="state"></a>狀態

類型： **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

您要設定其狀態的介面卡上狀態專案類型。 如需每個介面卡狀態種類的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

類型： **size_t**

您 (選擇性地) 配置並在 *inputStateDetails* 中提供的輸入狀態詳細資料緩衝區大小（以位元組為單位）。

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

類型： **void const \***

您在應用程式中配置的常數輸入狀態詳細資料緩衝區的選擇性指標，其中包含您在 [ *狀態*] 中指定之狀態類型所需的任何要求資訊。 如需特定狀態種類的任何輸入緩衝區需求的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。

### <a name="inputdatasize"></a>inputDataSize

類型： **size_t**

您在 *inputData* 中配置並提供之輸入緩衝區的大小（以位元組為單位）。

### <a name="inputdata-in"></a>inputData [in]

類型： **void \***

您在應用程式中配置之輸入緩衝區的指標，其中包含要針對您在 [ *狀態*] 中指定之狀態專案設定的狀態資訊。 如需特定狀態種類之輸入緩衝區需求的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|介面卡不再處於有效狀態。|
|DXGI_ERROR_INVALID_CALL|此作業系統 (OS) 無法辨識 *狀態* 中指定的狀態種類。 呼叫 [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) ，確認此介面卡和作業系統 (OS) 的設定狀態是否可用。|
|DXGI_ERROR_UNSUPPORTED|介面卡不支援 *狀態* 中指定的狀態種類。 呼叫 [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) ，確認此介面卡和作業系統 (OS) 的設定狀態是否可用。|
|E_INVALIDARG|提供的緩衝區大小不足以供 *inputData* (或 *inputStateDetails* ，其中需要輸入狀態詳細資料緩衝區) 。|
|E_POINTER|`nullptr` 提供給 *inputData* (或 *inputStateDetails* ，其中需要輸入狀態詳細資料緩衝區) 。|

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)