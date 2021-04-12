---
title: DXCoreAdapterState
description: 定義常數，指定 DXCore 介面卡狀態的種類。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315559"
---
# <a name="dxcoreadapterstate-enum"></a>DXCoreAdapterState 列舉

定義常數，指定 DXCore 介面卡狀態的種類。 將下列其中一個常數傳遞給 [IDXCoreAdapter：： QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) 方法，以取得狀態種類的介面卡狀態專案。將常數傳遞給 [IDXCoreAdapter：： SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) 方法，以設定狀態專案的介面卡資訊。

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>常數

### <a name="isdriverupdateinprogress"></a>IsDriverUpdateInProgress

指定 <em>IsDriverUpdateInProgress</em> 介面卡狀態，表示已在 `true` 介面卡上起始驅動程式更新，但尚未完成。 如果驅動程式更新已完成，則介面卡將會失效，而您的[QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)呼叫會傳回<b>DXGI_ERROR_DEVICE_REMOVED</b>的<b>HRESULT</b> 。

呼叫 [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)時， <em>IsDriverUpdateInProgress</em> 狀態專案的類型 <b>uint8_t</b>，代表布林值。

<b>重要</b>： 此狀態專案不支援 [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)。

### <a name="adaptermemorybudget"></a>AdapterMemoryBudget

指定可在介面卡上抓取或要求介面卡記憶體預算的 <em>AdapterMemoryBudget</em> 介面卡狀態。

呼叫 [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)時， <em>AdapterMemoryBudget</em>介面卡狀態具有 *inputStateDetails* 的類型 <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> ，以及 *DXCoreAdapterMemoryBudget* 的類型 <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">outputBuffer</a> 。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter：： QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md)、 [IDXCoreAdapter：： SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)