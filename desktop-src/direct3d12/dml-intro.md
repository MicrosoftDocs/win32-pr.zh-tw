---
title: DirectML 簡介
description: 直接機器學習 (DirectML) 是適用于機器學習 (ML) 的低層級 API。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 2dd37bc4c27364e26e4bbd4ae2cf5d43031c3314
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103786"
---
# <a name="introduction-to-directml"></a>DirectML 簡介

## <a name="summary"></a>總結

直接機器學習 (DirectML) 是適用于機器學習 (ML) 的低層級 API。 硬體加速機器學習服務基本 (稱為運算子) 是 DirectML 的構成要素。 您可以從這些構成要素開發像是消除倍增、消除鋸齒和樣式轉移等機器學習技術，以提供更多的名稱。 例如，Denoising 和超解析度，可讓您以較少的每圖元光線來達成令人印象深刻的 raytraced 效果。

您可以將機器學習推斷工作負載整合到您的遊戲、引擎、中介軟體、後端或其他應用程式中。 DirectML 具有熟悉的 (原生 c + +、nano COM) DirectX 12 樣式的程式設計介面和工作流程，並受到所有 DirectX 12 相容硬體的支援。 針對 DirectML 範例應用程式（包括基本 DirectML 應用程式的範例），請參閱 [DirectML 範例應用](dml-min-app.md)程式。

DirectML 是在 Windows 10 1903 版和對應版本的 Windows SDK 中引進。

## <a name="is-directml-appropriate-for-my-project"></a>DirectML 適用于我的專案嗎？

DirectML 是 [Windows Machine Learning](/windows/ai) 傘下的元件。 較高層級的 WinML API 主要是以模型為焦點，其具有負載系結-評估工作流程。 但是像遊戲和引擎這樣的網域通常需要較低層級的抽象層級，而開發人員可以使用較高程度的控制項，才能充分利用晶片。 如果您要計算毫秒數，並擠壓幀時間，則 DirectML 將符合您的機器學習需求。

針對可靠的即時、高效能、低延遲及/或資源限制的案例，請使用 DirectML (而非 WinML) 。 您可以將 DirectML 直接整合至現有的引擎或轉譯管線。 或者，在更高層級的自訂機器學習架構和中介軟體，DirectML 可以在 Windows 上提供高效能的後端。

WinML 本身會使用 DirectML 做為它的其中一個後端來執行。

## <a name="what-work-does-directml-do-and-what-work-must-i-do-as-the-developer"></a>DirectML 執行的工作有哪些;開發 *人員必須做* 什麼工作？

DirectML 會在 GPU (或 AI 加速核心（如果有) ）上，有效率地執行您推斷模型的個別層級。 每一層都是一個操作員，DirectML 可為您提供低層級、硬體加速機器學習基本運算子的程式庫。 這些運算子有專為其設計的硬體特定和架構特定的優化 (詳細說明 [DirectML 執行此作業的部分為何？](#why-does-directml-perform-so-well)) 。 同時，您的開發人員會看到一個與廠商無關的介面來執行這些運算子。

DirectML 中的運算子程式庫會提供您預期能夠在機器學習工作負載中使用的所有一般作業。

- 啟用運算子，例如 **線性**、 **ReLU**、 **sigmoid**、 **tanh** 等等。
- 專案取向運算子，例如 **add**、 **exp**、 **log**、 **max**、 **min**、 **sub** 等等。
- 卷積運算子，例如2D 和 3D **卷積** 等等。
- 減少運算子，例如 **argmin**、 **average**、 **l2**、 **sum** 等等。
- 共用運算子，例如 **average**、 **lp** 和 **max**。
- 類神經網路 (NN) 運算子，例如 **gemm**、 **gru**、 **lstm** 和 **rnn**。
- 還有更多。

為了達到最大效能，且您不需支付未使用的部分，DirectML 會將控制項放在您的手中，以開發人員瞭解如何在硬體上執行機器學習工作負載。 找出要執行的操作員，以及您身為開發人員的責任。 您可自行決定的工作包括：轉譯模型;簡化和優化您的層級;正在載入加權;資源配置、系結、記憶體管理 (就像使用 Direct3D 12) ;和圖形的執行。

您可以保留圖形的高階知識 (您可以直接對模型進行硬式編碼，也可以撰寫自己的模型載入器) 。 您可能會設計消除倍增模型，例如，每個 **upsample**、**卷積** **、正規化和****啟用** 運算子都使用數個層級。 藉由熟悉、謹慎排程和屏障管理，您就可以從硬體中解壓縮最多的平行處理原則和效能。 如果您正在開發遊戲，則您可以對排程進行謹慎的資源管理和控制，讓您能夠交錯機器學習工作負載和傳統的轉譯工作，以便讓 GPU 飽和。

## <a name="whats-the-high-level-directml-workflow"></a>高層級 DirectML 工作流程是什麼？

以下是我們預期如何使用 DirectML 的高階配方。 在初始化和執行的兩個主要階段中，您可以將工作記錄至命令清單，然後在佇列上執行它們。

### <a name="initialization"></a>初始化

1. 建立 direct3d 12 的資源 &mdash; ： direct3d 12 裝置、命令佇列、命令清單和資源（例如描述項堆積）。
2. 因為您正在執行機器學習推斷以及轉譯工作負載，所以請建立 &mdash; DirectML 裝置和操作員實例的 DirectML 資源。 如果您有機器學習模型，而您需要使用特定的資料類型，以特定的篩選 tensor 大小來執行特定類型的卷積，則這些都是 DirectML 的 **卷積** 運算子中的所有參數。
3. DirectML 記錄可用於 Direct3D 12 命令清單。 因此，完成初始化之後，您可以記錄 (的系結和初始化，例如，) 您的卷積運算子放入命令清單中。 然後，在佇列上關閉並執行您的命令清單（如同往常一樣）。

### <a name="execution"></a>執行

1. 將您的權數張量上傳至資源。 DirectML 中的 tensor 會使用一般 Direct3D 12 資源來表示。 例如，如果您想要將權數資料上傳至 GPU，那麼您可以使用與任何其他 Direct3D 12 資源相同的方式， (使用上傳堆積或複製佇列) 。
2. 接下來，您必須將這些 Direct3D 12 資源系結為您的輸入和輸出張量。 記錄到您的命令清單中，系結和操作員的執行。
3. 關閉並執行您的命令清單。

和 Direct3D 12 一樣，資源存留期和同步處理都是您的責任。 例如，請勿釋放您的 DirectML 物件，直到它們在 GPU 上完成執行為止。

## <a name="why-does-directml-perform-so-well"></a>為什麼 DirectML 執行得很好？

有一個很好的原因，就是您不應該只在 [計算著色器](/windows/desktop/direct3d12/pipelines-and-shaders-with-directx-12#direct3d-12-compute-pipeline)中撰寫自己的卷積運算子 (例如) 作為 HLSL。 使用 DirectML 的優點是， &mdash; 除了節省您自己 homebrewing 解決方案的優點之外， &mdash; 它還能提供您更好的效能，而不是使用手寫的一般用途計算著色器（如 **卷積** 或 **lstm**）來達成。

由於 Direct3D 12 metacommands 功能的緣故，DirectML 可達成這個部分。 Metacommands 會公開一小 DirectML 的功能，可讓硬體廠商提供 DirectML 對廠商硬體特定和架構特定優化的存取。 例如，多個運算子 &mdash; （例如，加總的上積） &mdash; 可以 *合併* 成單一 metacommand。 基於這些因素，DirectML 能夠超越更妥善撰寫、且專為在各種硬體上執行而撰寫的手動調整計算著色器的效能。

Metacommands 是 Direct3D 12 API 的一部分，不過它們是鬆散耦合的。 Metacommand 是由固定的 [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)所識別，而它的所有其他相關資訊 (從其行為和語義，到其簽章和名稱) 並不是 DIRECT3D 12 API 的一部分。 相反地，metacommand 是在其作者和執行它的驅動程式之間指定。 在此情況下，作者是 DirectML。 Metacommands 是 Direct3D 12 基本專案 (就像繪製和分派) 一樣，因此可以記錄到命令清單中並排程執行。

DirectML 使用整個機器學習 metacommands 套件來加速您的機器學習工作負載。 因此，您不需要撰寫廠商特定的程式碼路徑，就能為您的推斷達成硬體加速。 如果您在 AI 加速的晶片上執行，則 DirectML 會使用該硬體來大幅加速操作，例如卷積。 您可以採用您所撰寫的相同程式碼，而不需要修改它，在不是 AI 加速的晶片上執行 (可能是您膝上型電腦中的整合式 GPU) ，而且仍會獲得絕佳的 GPU 硬體加速。 如果沒有可用的 GPU，DirectML 就會回到 CPU。
