---
description: 為了驅動視覺效果更新，應用程式應該使用 IDirectManipulationCompositor。
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: 撰寫引擎
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 14bc2ad60405dba7874493096e022b553a8b276cd6f0bb21ea9ae3cf191f5d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117898"
---
# <a name="composition-engine"></a>撰寫引擎

為了驅動視覺效果更新，應用程式應該使用 [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)。 此物件負責根據[直接操作](direct-manipulation-portal.md)更新來更新視覺效果、推動慣性更新，並提供組合計時資訊給直接操作，而且應用程式應該使用[直接操作](direct-manipulation-portal.md)所提供的[DCompManipulationCompositor](direct-manipulation-guids.md) ，這將會代表應用程式處理所有的視覺效果更新，並驅動慣性更新。

[DCompManipulationCompositor](direct-manipulation-guids.md)是包裝 [DirectComposition](../directcomp/directcomposition-portal.md)之 [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)介面的實作為。 透過此組合器物件 [直接操作](direct-manipulation-portal.md) 可以直接在 DirectComposition 樹狀結構上設定轉換來套用輸出，而不是讓應用程式套用輸出。 藉由使用此設定，不論 UI 執行緒上的活動為何，都可以處理輸入並套用輸出轉換。

為了在組合引擎的時間提供 [直接操作](direct-manipulation-portal.md) 資訊， [DCompManipulationCompositor](direct-manipulation-guids.md) 類別會執行 [**IDirectManipulationFrameInfoProvider**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) 介面。 建立視口時，會針對 **IDirectManipulationFrameInfoProvider** 的實例，對從 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)取得的 [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)指標進行 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。 **IDirectManipulationFrameInfoProvider** 指標會傳遞至 [**IDirectManipulationManager：： CreateViewport ()**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport)函式。
