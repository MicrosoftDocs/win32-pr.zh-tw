---
description: Windows Installer 資料庫中的基本 InstalUISequence 資料表建議的動作順序。
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: 建議的 InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969400"
---
# <a name="suggested-installuisequence"></a>建議的 InstallUISequence



| 動作                                          | 條件                                                                                                  | 順序 |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| FatalErrorDlg                                   |                                                                                                            | -3       |
| UserExitDlg                                     |                                                                                                            | -2       |
| ExitDlg                                         |                                                                                                            | -1       |
| [LaunchConditions](launchconditions-action.md) |                                                                                                            | 100      |
| PrepareDlg                                      |                                                                                                            | 140      |
| [AppSearch](appsearch-action.md)               |                                                                                                            | 400      |
| [CCPSearch](ccpsearch-action.md)               | 未 [**安裝**](installed.md)                                                                         | 500      |
| [RMCCPSearch](rmccpsearch-action.md)           | 未 [**安裝**](installed.md)                                                                         | 600      |
| [CostInitialize](costinitialize-action.md)     |                                                                                                            | 800      |
| [FileCost](filecost-action.md)                 |                                                                                                            | 900      |
| [CostFinalize](costfinalize-action.md)         |                                                                                                            | 1000     |
| WelcomeDlg                                      | 未 [**安裝**](installed.md)                                                                         | 1230     |
| ResumeDlg                                       | [**已安裝**](installed.md) 和 ( [**繼續**](resume.md) 或 [**預先**](preselected.md) 選取)        | 1240     |
| MaintenanceWelcomeDlg                           | [**已安裝**](installed.md)且不會 [**繼續**](resume.md)，也不會 [**預先**](preselected.md)選取 | 1250     |
| ProgressDlg                                     |                                                                                                            | 1280     |
| [ExecuteAction](executeaction-action.md)       |                                                                                                            | 1300     |



 

 

 



