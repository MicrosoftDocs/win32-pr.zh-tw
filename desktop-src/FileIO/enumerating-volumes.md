---
description: 若要在電腦上建立磁片區的完整清單，或輪流操作每個磁片區，您可以列舉磁片區。
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: 列舉磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975756"
---
# <a name="enumerating-volumes"></a>列舉磁片區

若要在電腦上建立磁片區的完整清單，或輪流操作每個磁片區，您可以列舉磁片區。 在磁片區中，您可以掃描磁片區上 [裝載的資料夾](enumerating-volume-mount-points.md) 或其他物件。

有三個功能可讓應用程式列舉電腦上的磁片區：

-   [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

這三個函式的運作方式非常類似 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)和 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數。

開始使用 [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)來搜尋磁片區。 如果搜尋成功，請根據應用程式的設計來處理結果。 然後，在迴圈中使用 [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) 來找出並處理每個後續的磁片區。 當磁片區的供應時間用盡時，請關閉 [使用 [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)搜尋]。

您不應該假設這些函式所傳回之磁片區的順序與其他函式或工具傳回的磁片區順序之間的任何關聯性。 尤其是，如果有任何) 或磁片系統管理員，則不會假設 (的磁片區順序和磁碟機號之間的任何關聯性，以及 BIOS 所指派的磁碟機號。

如需如何列舉電腦上的磁片區的範例，請參閱 [裝載的資料夾範例](volume-mount-point-examples.md) 。

 

 



