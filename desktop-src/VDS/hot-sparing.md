---
description: 熱備份
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: 熱備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b8df9bc27e303277c869901872a9b879cb2d7df32764589501b9d33a51c3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125948"
---
# <a name="hot-sparing"></a>熱備份

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

熱備份是磁片或磁片磁碟機故障或磁片磁碟機故障或磁片磁碟機的替代磁片磁碟機。  (硬體提供者對磁片磁碟機採取行動;軟體提供者可在磁片上運作。 ) 您可以在子系統中的所有 Lun 之間共用熱備用磁片磁碟機，或將其與特定 LUN 建立關聯。 同樣地，您可以將熱備用磁片與單一磁片區、套件和軟體提供者建立關聯，或在 SAN 上的所有主機之間共用。

如果相關聯的磁片區或 LUN 具有容錯功能，您可以用熱備用空間來取代故障的磁片或磁片磁碟機，並重建任何受影響的同位 RAID 或鏡像。 即使相關聯的磁片區或 LUN 無法容錯，您也可以更換故障磁片的熱備用。 假設您可以在發生重大資料遺失之前判斷即將發生的失敗，您可以暫時將熱備用映射鏡像至故障的磁片或磁片磁碟機，然後移除故障的磁片或磁片磁碟機。

熱備用可以是自動或手動。 如果提供者會執行自動熱備份，它會動態地執行替代。 手動熱備份需要操作員或應用程式介入。 熱備用可以包含部分資料或從先前使用的格式。 發生替代時，VDS 會覆寫熱備用。

您無法使用熱備用來進行一般系結作業。 如果熱備件大於失敗的磁片或磁片磁碟機，則任何多餘的空間都會保持未使用，直到明確宣告可供系結使用為止。 使用熱備用復原後，磁片或磁片磁碟機就不再是熱備用。 換句話說，1 16 gb 主軸無法作為 2 8 gb 的熱備件。

 

 
