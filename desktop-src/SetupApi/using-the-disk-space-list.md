---
description: 您必須先使用 SetupCreateDiskSpaceList 函式來建立檔案作業，才能從磁碟空間清單中新增或移除檔案作業。
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: 使用 Disk-Space 清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978914"
---
# <a name="using-the-disk-space-list"></a>使用 Disk-Space 清單

您必須先使用 [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) 函式來建立檔案作業，才能從磁碟空間清單中新增或移除檔案作業。

建立磁碟空間清單之後，您可以使用 [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)，將個別的檔案複製或刪除作業新增至清單。 若要在整個 INF 區段中新增所有檔案複製或刪除作業，請使用 [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) 或 [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) 函數。

將所有安裝操作新增到磁碟空間清單之後，您可以使用 [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) 函式來查詢它，以找出指定安裝所需的磁碟空間量。

[**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)函式會傳回磁碟空間清單上，檔案作業中所參考之每個目標磁片磁碟機的磁片磁碟機規格。 您可以使用這項資訊，以程式設計方式將這些磁片磁碟機上的可用空間與安裝所需的空間進行比較。

若要從磁碟空間清單中移除檔案作業，請使用 [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) 函數。 若要從整個 INF 區段中移除所有檔案複製或刪除作業，請使用 [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) 或 [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) 函數。

不再需要磁碟空間清單之後，您可以藉由呼叫 [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) 函式來釋放配置給它的資源。

 

 



