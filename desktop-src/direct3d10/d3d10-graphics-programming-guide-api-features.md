---
description: Direct3D 10 圖形管線代表基本的架構變更，從硬體和軟體的基礎中重建，以增強下一代的遊戲和3D 多媒體應用程式。
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: " (Direct3D 10) 的 API 功能"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 416018fcddf2643ba9fbc8e633ec2f636b8158ff329780a55205034e5dbbe240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858658"
---
# <a name="api-features-direct3d-10"></a> (Direct3D 10) 的 API 功能

Direct3D 10 圖形管線代表基本的架構變更，從硬體和軟體的基礎中重建，以增強下一代的遊戲和3D 多媒體應用程式。 它會使用 Windows 顯示驅動程式模型 (WDDM) ，以啟用效能和行為增強功能，例如虛擬 GPU 記憶體。

熟悉 Direct3D 9 的開發人員將探索 Direct3D 10 中一系列的功能增強功能和效能改進，包括：

-   在新 [幾何著色器階段](/previous-versions//bb205146(v=vs.85))中處理整個基本專案的能力。
-   使用 [資料流程輸出階段](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md)將管線產生的頂點資料輸出至記憶體的能力。
-   將管線狀態組織成5個不可變的 [狀態物件](d3d10-graphics-programming-guide-api-features-state-objects.md)，以便快速設定管線。
-   將著色器常陣列織成 [常數緩衝區](d3d10-graphics-programming-guide-resources-types.md)，將提供著色器常數資料的頻寬負荷降至最低。
-   使用幾何著色器來執行每個基本材質交換和設定的能力。
-   新的 [資源類型](d3d10-graphics-programming-guide-resources-types.md) (包括可從著色器) 和資源格式編制索引的材質陣列。
-   使用 [view](d3d10-graphics-programming-guide-resources-access-views.md)提高資源存取的一般化。
-   舊版硬體功能位 (caps) 已移除，以提供一組豐富的保證功能，其目標為 Direct3D 10 類別的硬體 (最小) 。
-   [分層運行](d3d10-graphics-programming-guide-api-features-layers.md) 時間-DIRECT3D 10 API 是以核心的基本功能來建立，並建立選擇性和開發人員協助工具 (debug 等 ) 在外部層中。
-   完整的 HLSL 整合-所有 Direct3D 10 著色器都會以 HLSL 撰寫，並以 [一般著色器核心](../direct3dhlsl/dx-graphics-hlsl-common-core.md)來執行。
-   轉譯目標、紋理和取樣器數目的增加。 也沒有任何著色器長度限制。
-   整數和位著色器作業。
-   Readback 深度/樣板表面或多重取樣資源不再系結為轉譯目標。
-   多重取樣 Alpha 到涵蓋範圍支援。

Direct3D 9 開發人員也應該注意其他的行為差異， (請參閱 [direct3d 9 至 direct3d 10 考慮](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)) 。

以下是已不再支援的 Direct3D 9 功能清單，或已在 Direct3D 10 中修改過的 Direct3D 9 功能 (參閱已 [淘汰的功能](d3d10-graphics-programming-guide-api-features-deprecated.md)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 10 程式設計手冊](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
