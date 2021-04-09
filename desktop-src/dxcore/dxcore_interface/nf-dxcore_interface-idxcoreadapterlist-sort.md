---
title: IDXCoreAdapterList::Sort
description: 根據提供的排序準則輸入陣列來排序 DXCore 介面卡清單物件。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093155"
---
# <a name="idxcoreadapterlistsort-method"></a>IDXCoreAdapterList：： Sort 方法

## <a name="description"></a>Description

根據提供的排序準則輸入陣列排序 DXCore 介面卡清單物件，其中較早在準則陣列中的陣列專案會獲得較高的加權。 **排序** 可協助您更輕鬆地在介面卡清單中尋找理想的介面卡。

## <a name="syntax"></a>語法

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a>參數

### <a name="numpreferences"></a>numPreferences

類型： **uint32_t**

*喜好* 設定參數所指向之陣列中的元素數目。

### <a name="preferences-in"></a>喜好設定 [in]

Type： **Const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)值之常數陣列的指標，代表排序準則。

## <a name="returns"></a>傳回

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。

|傳回值|描述|
|-|-|
|E_INVALIDARG|*NumPreferences* 引數為零，或 *喜好* 設定引數為 `nullptr` 。|

## <a name="remarks"></a>備註

如果作業系統 (OS) 無法辨識提供的 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值，則會予以忽略，而不會導致 API 失敗。 在此情況下，仍會考慮已知的 **DXCoreAdapterPreference** 值。 若要判斷 API 是否可理解排序類型，請呼叫 [IDXCoreAdapterList：： IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)。

稍早在提供的 *喜好* 設定陣列中所發生的 **DXCoreAdapterPreference** 值會被視為較高的優先順序。 

如需每個類型所套用邏輯的詳細資訊，請參閱 **DXCoreAdapterPreference** 列舉檔。 型別的內部邏輯可能會隨著作業系統開發而開發。

當 **排序** 傳回時，DXCore 介面卡清單中的專案會從最慣用到最不理想的順序排序。 因此，以索引0呼叫 [IDXCoreAdapterList：： GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) 會抓取最符合所要求之排序喜好設定類型的介面卡;索引1是下一個最相符的結果，依此類推。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)