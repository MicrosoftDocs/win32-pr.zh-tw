---
description: 虛擬機器相關的虛擬化 WMI 類別。
ms.assetid: 1BD64741-C316-4E74-B0AB-4E595C77FD91
title: 虛擬系統類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b67464c8a8e0a7c738685207e58396d4777cee9eb875c1d5f6879c665d5aa44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765538"
---
# <a name="virtual-system-classes"></a>虛擬系統類別

以下是與虛擬機器相關的虛擬化 WMI 類別。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ BootSourceComponent**](msvm-bootsourcecomponent.md)<br/>                             | 將 [**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md) 與整體 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)建立關聯。 <br/>                                                                                                                                                                                                                                                   |
| [**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md)<br/>                         | 代表用來設定虛擬機器開機來源的參數。 <br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Msvm \_**](msvm-computersystem.md)<br/>                                       | 代表實體電腦系統或虛擬機器。<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| [**Msvm \_ ConcreteComponent**](msvm-concretecomponent.md)<br/>                                 | 用來在 managed 元素之間建立「部分」關聯性的泛型關聯。<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**Msvm \_ LogicalIdentity**](msvm-logicalidentity.md)<br/>                                     | 將兩個代表相同基礎實體不同層面的 managed 專案產生關聯。 <br/>                                                                                                                                                                                                                                                                                                                            |
| [**Msvm \_ MostCurrentSnapshotInBranch**](msvm-mostcurrentsnapshotinbranch.md)<br/>             | 將代表虛擬系統之 [**Msvm \_**](msvm-computersystem.md) 系統的實例或 [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) 類別的實例，與代表相依快照集中最新快照集之虛擬系統快照集的 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別的實例產生關聯。<br/>            |
| [**Msvm \_ ParentChildSettingData**](msvm-parentchildsettingdata.md)<br/>                       | [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)實例與 **Msvm \_ VirtualSystemSettingData** 實例之間的關聯，代表這個物件所依據的最新快照集。<br/>                                                                                                                                                                                 |
| [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)<br/>                         | 代表已規劃的虛擬機器。<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| [**Msvm \_ SnapshotOfVirtualSystem**](msvm-snapshotofvirtualsystem.md)<br/>                     | 將虛擬系統與從虛擬系統所捕獲的快照集產生關聯。<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)<br/>                               | 用於 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別中的 [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)和 [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md)方法，以快速取得與虛擬機器或快照集相關的一般資訊。<br/> |
| [**Msvm \_ SystemComponent**](msvm-systemcomponent.md)<br/>                                     | 建立系統與其組成之任何 managed 系統專案之間的「部分」關聯性。<br/>                                                                                                                                                                                                                                                                                                               |
| [**Msvm \_ SystemDevice**](msvm-systemdevice.md)<br/>                                           | 將邏輯裝置與父系統產生關聯。<br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**Msvm \_ VirtualSystemCapabilities**](msvm-virtualsystemcapabilities.md)<br/>                 | 描述相關聯 Msvm 的非 [**程式 \_**](msvm-computersystem.md)的功能。<br/>                                                                                                                                                                                                                                                                                                                           |
| [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)<br/>                   | 代表虛擬機器的虛擬化特定設定。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**Msvm \_ VirtualSystemSettingDataComponent**](msvm-virtualsystemsettingdatacomponent.md)<br/> | 泛型關聯，用來建立一個 [**cim \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 實例與一或多個 [**cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)實例之間的「部分」關聯性。<br/>                                                                                                                                                 |



 

 

