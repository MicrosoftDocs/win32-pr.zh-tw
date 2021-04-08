---
title: Windows Defender 結構
description: 應用程式在呼叫以要求掃描、簽章更新或 Windows Defender 的資訊時，所使用的結構。
ms.assetid: EF4116D3-DA50-4078-A024-2D624945D8C1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d690de552137ce267b9d1d7a9cec711b161528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672171"
---
# <a name="windows-defender-structures"></a>Windows Defender 結構

應用程式在呼叫以要求掃描、簽章更新或 Windows Defender 的資訊時，所使用的結構。



| 結構                                                      | Description                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MPCALLBACK \_ 資料**](mpcallback-data.md)                    | 傳遞至回呼函數的資料。<br/>                                        |
| [**MPCLEAN \_ 資料**](mpclean-data.md)                          | 傳遞給清除回呼函數的通知資料。<br/>                         |
| [**MPCLEAN 前置檢查 \_ \_ 資料**](mpclean-precheck-data.md)       | 傳遞給清除前置檢查回呼函數的通知資料。<br/>                |
| [**MPCOMPONENT \_ 狀態**](mpcomponent-status.md)              | 元件狀態資訊。<br/>                                                |
| [**MPCOMPONENT \_ 版本**](mpcomponent-version.md)            | 個別元件的版本和更新時間。<br/>                         |
| [**MPCONFIGURATION \_ 資料**](mpconfiguration-data.md)          | 包含設定變更的相關資料，包括舊值和新值。<br/> |
| [**MPENDOFLIFE \_ 資料**](mpendoflife-data.md)                  | 「生命週期結束」通知資料。<br/>                                             |
| [**MPEXPIRATION \_ 資料**](mpexpiration-data.md)                | 產品到期狀態通知。<br/>                                      |
| [**MPFASTPATH \_ 資料**](mpfastpath-data.md)                    | FastPath 更新通知。<br/>                                                |
| [**MPHEALTH \_ 資料**](mphealth-data.md)                        | 健康情況通知資料。<br/>                                                    |
| [**MPMALWARETOAST \_ 資料**](mpmalwaretoast-data.md)            | 惡意程式碼快顯通知資料。<br/>                                             |
| [**MPNIS \_ 私用 \_ 資料**](mpnis-private-data.md)             | 私人 NIS 通知。<br/>                                                   |
| [**MPRESERVED \_ 資料**](mpreserved-data.md)                    | 保留的通知資料。<br/>                                                  |
| [**MPRESOURCE \_ 資訊**](mpresource-info.md)                    | 資源資訊結構。<br/>                                              |
| [**MPRESOURCE \_ 統計資料**](mpresource-stats.md)                  | 與資源相關的統計資料。<br/>                                                 |
| [**MPSAMPLE \_ 資料**](mpsample-data.md)                        | 傳遞給範例提交回呼函數的通知資料。<br/>         |
| [**MPSCAN \_ 資料**](mpscan-data.md)                            | 掃描傳遞給回呼的資料。<br/>                                            |
| [**MPSCAN \_ 資源**](mpscan-resources.md)                  | 掃描操作期間傳遞的資源資訊。<br/>                         |
| [**MPSCAN \_ 結果**](mpscan-result.md)                        | 掃描的結果。<br/>                                                       |
| [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md)                  | 傳遞至簽章更新回呼函數的通知資料。<br/>          |
| [**MPSTATUS \_ 資料**](mpstatus-data.md)                        | 包含產品元件目前狀態的相關資料。<br/>        |
| [**\_ \_ 未使用的 MPSTATUS DATAEX**](mpstatus-dataex-unused.md)     | 非 SRP 的虛擬結構。<br/>                                                 |
| [**MPSTATUS \_ 資訊**](mpstatus-info.md)                        | 惡意程式碼防護管理員的狀態資訊。<br/>                       |
| [**MPTHREAT \_ 資料**](mpthreat-data.md)                        | 因為威脅偵測或修改而傳遞的通知資料。<br/>            |
| [**MPTHREAT \_ 資訊**](mpthreat-info.md)                        | 包含威脅的相關資訊。<br/>                                         |
| [**MPTHREAT \_ INFOEX \_ 行為**](mpthreat-infoex-behavior.md) | 包含行為修改特定的資訊。<br/>                         |
| [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)           | 包含 NIS 特定的資訊。<br/>                                           |
| [**\_ \_ 未使用的 MPTHREAT INFOEX**](mpthreat-infoex-unused.md)     | 非行為修改類型威脅的虛擬結構。<br/>                  |
| [**MPTHREAT \_ 當地語系化的 \_ 資訊**](mpthreat-localized-info.md)   | 威脅的當地語系化資訊。<br/>                                          |
| [**MPTHREAT \_ 統計資料**](mpthreat-stats.md)                      | 威脅相關的統計資料。<br/>                                                   |
| [**MPTHREAT \_ 統計 \_ 資料**](mpthreat-stats-data.md)           | 其他威脅統計資料資料。<br/>                                           |
| [**MPVERSION \_ 資訊**](mpversion-info.md)                      | 惡意程式碼防護管理員元件的版本資訊。<br/>         |



 

 

 





