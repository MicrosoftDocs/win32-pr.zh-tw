---
title: IDXCoreAdapter
description: " **IDXCoreAdapter**   介面會執行方法，以取得介面卡專案的詳細資料。"
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093152"
---
# <a name="idxcoreadapter-interface"></a>IDXCoreAdapter 介面

 **IDXCoreAdapter**   介面會執行方法，以取得介面卡專案的詳細資料。 **IDXCoreAdapter** 繼承自 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="remarks"></a>備註

介面卡的屬性會在介面卡啟動時建立，而且在介面卡的存留期內是不可變的。 這與可查詢或設定的介面卡狀態不同，而其值可能會隨著時間而變更。

## <a name="see-also"></a>另請參閱

[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)