---
description: Integration services 是一項軟體服務，可在子虛擬機器內的客體作業系統上執行，並作為管理作業系統中虛擬化堆疊的一部分，以提供與管理作業系統的某種程度的整合。
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Integration services 類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04d60a913159c49387848b5e18a3e37b942f3e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512796"
---
# <a name="integration-services-classes"></a>Integration services 類別

Integration services 是一項軟體服務，可在子虛擬機器內的客體作業系統上執行，並作為管理作業系統中虛擬化堆疊的一部分，以提供與管理作業系統的某種程度的整合。 它們是用來解決虛擬機器所提供的高階隔離所產生的問題。

以下是與 integration services 相關的虛擬化 WMI 類別。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                | 描述                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)<br/>                                               | 代表來賓檔案服務作業。 <br/>                                                                                                                                                                                                            |
| [**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)<br/>                               | 代表將檔案從主機複製到來賓的參數。 <br/>                                                                                                                                                                                |
| [**Msvm \_ GuestFileService**](msvm-guestfileservice.md)<br/>                                                   | [**Msvm \_GuestFileService**](msvm-guestfileservice.md) 包含可用於將檔案從 hyper-v 主機複製到虛擬機器的方法。 <br/>                                                                                                     |
| [**Msvm \_ GuestService**](msvm-guestservice.md)<br/>                                                           | [**Msvm \_GuestService**](msvm-guestservice.md) 是來賓中可從主機存取之服務的抽象基類。 <br/>                                                                                                                  |
| [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)<br/>                       | 代表來賓服務介面元件的狀態，它提供了一種機制，可讓您從主機系統上的管理介面與虛擬機器進行互動。 <br/>                                                                         |
| [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | 代表來賓服務介面元件的設定狀態。 <br/>                                                                                                                                                                                 |
| [**Msvm \_ KvpExchangeComponent**](msvm-kvpexchangecomponent.md)<br/>                                           | 代表索引鍵/值組 exchange 服務的狀態，此服務提供一種機制，可在虛擬機器與管理作業系統上執行的作業系統之間交換資料。<br/>                                                  |
| [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | 代表索引鍵/值組 exchange 服務的設定狀態。<br/>                                                                                                                                                                                    |
| [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)<br/>                                             | 代表索引鍵/值組。<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ RegisteredGuestService**](msvm-registeredguestservice.md)<br/>                                       | 代表 [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) 實例與 [**Msvm \_ GuestService**](msvm-guestservice.md)實例之間的關聯，代表在來賓中執行的服務。 <br/> |
| [**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)<br/>                                                 | 代表關機服務的狀態，此服務提供從主機系統的管理介面關閉虛擬機器作業系統的機制。<br/>                                                                       |
| [**Msvm \_ ShutdownComponentSettingData**](msvm-shutdowncomponentsettingdata.md)<br/>                           | 代表關機服務的設定狀態。<br/>                                                                                                                                                                                                   |
| [**Msvm \_ TimeSyncComponent**](msvm-timesynccomponent.md)<br/>                                                 | 代表時間同步處理服務的狀態，此服務負責同步處理虛擬機器的系統時間與管理作業系統中執行之作業系統的系統時間。<br/>                             |
| [**Msvm \_ TimeSyncComponentSettingData**](msvm-timesynccomponentsettingdata.md)<br/>                           | 表示時間同步處理服務的設定狀態。<br/>                                                                                                                                                                                       |
| [**Msvm \_ VssComponent**](msvm-vsscomponent.md)<br/>                                                           | 代表磁碟區陰影複製服務 (VSS) 服務的狀態，此服務會在客體作業系統中執行 VSS 要求者。<br/>                                                                                                                    |
| [**Msvm \_ VssComponentSettingData**](msvm-vsscomponentsettingdata.md)<br/>                                     | 代表磁碟區陰影複製服務 (VSS) 服務的設定狀態。<br/>                                                                                                                                                                           |



 

 

 




