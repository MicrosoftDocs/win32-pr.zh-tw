---
description: 下列函式會搭配磁碟空間清單使用。
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Disk-Space 清單函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e20e6f656110cc3b8c2ebd607f28b5d701ce3007b4ce8812f7e3bcad2f7f5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887364"
---
# <a name="disk-space-list-functions"></a>Disk-Space 清單函數

下列函式會搭配磁碟空間清單使用。



| 函式                                                                                         | 描述                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | 調整指定磁片磁碟機所需的空間量。                                                                          |
| [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | 建立磁碟空間清單，並將資源配置給它。                                                                             |
| [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | 終結磁碟空間清單，釋放配置給它的資源。                                                                   |
| [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | 將磁碟空間清單複製為新的獨立磁碟空間清單。                                                                   |
| [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | 針對 [磁碟空間] 清單中所列的所有磁片磁碟機，以磁片磁碟機規格填滿緩衝區。                                       |
| [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | 傳回在 [磁碟空間] 清單中所列的特定磁片磁碟機上完成檔案作業所需的磁碟空間總量。 |
| [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | 將檔案複製或刪除操作新增至磁碟空間清單。                                                                         |
| [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | 將 INF 檔案的 [ **複製** 檔案] 或 [ **刪除** 檔案] 區段中的所有檔案作業新增至磁碟空間清單。                    |
| [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | 將 INF 檔案的 [ **安裝** ] 區段中的所有檔案作業新增至 [磁碟空間] 清單。                                        |
| [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | 從磁碟空間清單中移除檔案複製或刪除操作。                                                                      |
| [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | 從磁碟空間清單中移除 INF 檔案的 [ **複製** 檔案] 或 [ **刪除** 檔案] 區段中的所有檔案作業。               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | 從磁碟空間清單中移除 INF 檔案的 [ **安裝** ] 區段中的所有檔案作業。                                  |



 

 

 



