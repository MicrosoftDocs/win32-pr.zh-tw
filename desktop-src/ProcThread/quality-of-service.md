---
description: 服務品質表示執行緒的效能和電源效率，這可能會影響執行緒排程和處理器電源管理。
title: 服務品質
ms.topic: article
ms.date: 07/09/2021
ms.openlocfilehash: c506e810bafad41e9a5f14112c1398b0d6fb3ffc
ms.sourcegitcommit: 2805e19a2738a408d3c5ab69a8d84ec92ca25e36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/14/2021
ms.locfileid: "113989787"
---
# <a name="quality-of-service"></a>服務品質

與執行緒相關聯的服務品質 (QoS) 用來指出所需的效能和電源效率。 每個執行緒都會指派給 QoS 層級。 雖然排程優先權仍是系統決定接下來要排程之執行緒的主要度量，但 QoS 可能會影響核心選取和處理器電源管理。 在具有異類處理器的平臺上，執行緒的 QoS 可能會將排程限制在處理器的子集，或表示特定處理器類別的喜好設定。

開發人員可能已採用其他設備來控制何時執行，例如，使用者不存在時、只有在 AC/收費上，或根據電池計量。 QoS 提供了一種影響如何執行的設備。 此設備可協助改善 CPU 效率，進而延長電池壽命。 此外，此程式可協助降低 CPU 電源耗用量，並在使用 AC 電源來減少可能導致高風扇雜訊或甚至熱節流的熱輸出。

## <a name="quality-of-service-levels"></a>服務等級品質

系統會維護多個 QoS 層級，而每個層級都有差異的效能和電源效率。 Windows 針對每個 QoS 層級提供排程和處理器電源管理的標準預設設定。 您可以透過 Windows 布建來修改每個 QoS 層級的處理器電源管理和異類排程的精確調整。 如需效能微調和布建的詳細資訊，請參閱 [處理器電源管理選項](/windows-hardware/customize/power-settings/configure-processor-power-management-options)。

| QoS 層級 | Description|效能和威力 | 版本 |
| --- | --- | --- | --- |
| 高 | 以視窗化的應用程式，其位於前景和焦點，或可聽見 | 標準高效能 |1709 |
| 中 | 可對終端使用者顯示但不在焦點中的視窗化應用程式 | 依平臺而異，介於高與低 | 1709 |
| 低 | 以視窗化的應用程式，對使用者而言看不到或無法聽見 | 在電池上，選取最有效率的 CPU 頻率和排程來提高核心 | 1709 |
| 生態 | 使用[SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)以[SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)或執行緒明確標記進程的應用程式 | 一律為有效率的核心選取最有效率的 CPU 頻率和排程 | Windows 11 |
| 媒體 | 由 [多媒體類別](/windows/desktop/procthread/multimedia-class-scheduler-service) 排程器服務明確標記以表示多媒體批次緩衝的執行緒 | 降低 CPU 頻率以有效率地處理批次處理 | 2004 |
| 期限 | 由 [多媒體類別](/windows/desktop/procthread/multimedia-class-scheduler-service) 排程器服務明確標記的執行緒，表示音訊執行緒需要效能才能符合期限 | 符合媒體期限的高效能 | 2004 |

## <a name="quality-of-service-classification"></a>服務分類品質

下表顯示支援的 QoS 分類。

| 來源 | 描述 |
| --- | --- |
| 多媒體基礎 | [多媒體類別](/windows/desktop/procthread/multimedia-class-scheduler-service)排程器服務會排定多媒體案例的 CPU 資源。 服務會將負責多媒體處理的特定執行緒標記為使用媒體和期限 QoS 層級，以提供電源效率，同時符合效能期限。  |
| API | [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)可讓開發人員藉由切換 ProcessPowerThrottling 中的功能，將進程明確標記為 HighQoS 或 EcoQoS `PROCESS_POWER_THROTTLING_EXECUTION_SPEED` 。 </br>[SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)可讓開發人員藉由切換 ThreadPowerThrottling 中的功能，將執行緒明確標記為 HighQoS 或 EcoQoS `THREAD_POWER_THROTTLING_EXECUTION_SPEED` 。   |
| 發聲 | 決定要播放音訊的進程會 HighQoS。 |
| 可見 | 直接擁有視窗的進程 (或屬於視窗擁有進程的下階，) 會根據其可見度和焦點狀態指派 QoS 層級：</br></br><table><tr><th>視窗狀態</th><th>服務品質</th></tr><tr><td>聚焦</td><td>高</td></tr><tr><td>可見</td><td>中</td></tr><tr><td>最小化或完全 Pixels occluded</td><td>低</td></tr></table> |
| 啟發式 | 未由上述來源分類的執行緒會由系統自動指派 QoS 層級。 這些啟發學習法包含 (但不限於) 執行緒優先順序，其中以降低執行緒優先順序執行的執行緒可以表示較低的 QoS 層級。 |
