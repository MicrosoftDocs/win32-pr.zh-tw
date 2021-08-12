---
description: Windows Installer 資料庫中的基本 InstalUISequence 資料表建議的動作順序。
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: 建議的 InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab5c65ed594cf86f86555de235d0ceb0530b9f3e233bfdf5c38d094ca9719a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624330"
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



 

 

 



