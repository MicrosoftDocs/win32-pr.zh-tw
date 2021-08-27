---
title: IDXCoreAdapter::QueryState
description: 抓取介面卡上所指定專案的目前狀態。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2e5c585c249141c1491ddf36ee798d8b11148425026e9011bd0653169f998fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117718"
---
# <a name="idxcoreadapterquerystate-method"></a>IDXCoreAdapter：： QueryState 方法

抓取介面卡上所指定專案的目前狀態。 在呼叫屬性類型的 **QueryState** 之前，請先呼叫 [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) ，確認此介面卡與作業系統 (OS) 可以使用此狀態種類。

## <a name="syntax"></a>語法

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a>參數

### <a name="state"></a>狀態

類型： **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

介面卡上您想要取得其狀態的狀態專案類型。 如需每個介面卡狀態種類的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

類型： **size_t**

您 (選擇性地) 配置並在 *inputStateDetails* 中提供的輸入狀態詳細資料緩衝區大小（以位元組為單位）。

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

類型： **void const \***

您在應用程式中配置的常數輸入狀態詳細資料緩衝區的選擇性指標，其中包含您在 [ *狀態*] 中指定之狀態類型所需的任何要求資訊。 如需特定狀態種類的任何輸入緩衝區需求的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。

### <a name="outputbuffersize"></a>outputBufferSize

類型： **size_t**

您在 *outputBuffer* 中配置並提供之輸出緩衝區的大小（以位元組為單位）。

### <a name="outputbuffer-out"></a>outputBuffer [out]

類型： **void \***

您在應用程式中配置的輸出緩衝區指標，且該函式會填入。 如需特定狀態種類之輸出緩衝區需求的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|介面卡不再處於有效狀態。|
|DXGI_ERROR_INVALID_CALL|此作業系統 (OS) 無法辨識 *狀態* 中指定的狀態種類。 呼叫 [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) 確認此介面卡與作業系統 (OS) 可以使用查詢狀態種類。|
|DXGI_ERROR_UNSUPPORTED|介面卡不支援 *狀態* 中指定的狀態種類。 呼叫 [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) 確認此介面卡與作業系統 (OS) 可以使用查詢狀態種類。|
|E_INVALIDARG|提供的緩衝區大小不足以供 *outputBuffer* (或 *inputStateDetails* ，其中需要輸入狀態詳細資料緩衝區) 。|
|E_POINTER|`nullptr` 提供給 *outputBuffer* (或 *inputStateDetails* ，其中需要輸入狀態詳細資料緩衝區) 。|

## <a name="remarks"></a>備註

如需每個介面卡狀態種類的詳細資訊，以及使用的輸入和輸出，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 。 在填入之前，此函式會將 *outputBuffer* 緩衝區設為零。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)