---
title: DXCoreAdapterMemoryBudget
description: 描述介面卡的記憶體預算。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2cbe109d4c7f6c03389ec9e51c9468c601730890220fde2dea72aed476093f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118682"
---
# <a name="dxcoreadaptermemorybudget-structure"></a>DXCoreAdapterMemoryBudget 結構

指定可在介面卡上抓取或要求介面卡記憶體預算的 <em>AdapterMemoryBudget</em> 介面卡狀態。 設定要求) 預算的 (代表要在介面卡上保留的最小實體記憶體（以位元組為單位）。 建議您設定介面卡保留區，以代表您的應用程式在沒有的情況下無法移出的實體記憶體數量。 此值可協助作業系統 (作業系統) ，快速將大型記憶體壓力情況的影響降到最低。

呼叫 [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)時， <em>AdapterMemoryBudget</em>介面卡狀態具有 *inputStateDetails* 的類型 <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> ，以及 *DXCoreAdapterMemoryBudget* 的類型 **outputBuffer** 。

呼叫 [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)時， <em>AdapterMemoryBudget</em>介面卡狀態具有 *inputStateDetails* 的類型 <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> ，以及 *inputData* 的類型 **uint64_t** 。

## <a name="syntax"></a>語法

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a>成員

### <a name="budget"></a>預算

類型： **uint64_t**

以位元組為單位，指定您的應用程式應鎖定的 OS 提供的介面卡記憶體預算（以位元組為單位）。 如果 *currentUsage* 大於 *預算*，則您的應用程式可能會因為 OS 的背景活動而產生間斷情形或效能上的負面影響，這是為了讓其他應用程式能夠公平使用介面卡記憶體。

### <a name="currentusage"></a>currentUsage

類型： **uint64_t**

指定應用程式目前的介面卡記憶體使用量（以位元組為單位）。

### <a name="availableforreservation"></a>availableForReservation

類型： **uint64_t**

指定您的應用程式可用於保留的介面卡記憶體量（以位元組為單位）。 若要保留此介面卡記憶體，您的應用程式應該呼叫 [IDXCoreAdapter：： SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) ，並將 *狀態* 設定為 [DXCoreAdapterState：： AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)。

### <a name="currentreservation"></a>currentReservation

類型： **uint64_t**

指定應用程式所保留的介面卡記憶體量（以位元組為單位）。 OS 會使用保留做為提示，判斷應用程式的最小工作集。 您的應用程式應嘗試確定其介面卡的記憶體使用量可進行修剪，以符合此需求。

## <a name="see-also"></a>另請參閱

[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)