---
description: 存取指定磁片區上的檔案和目錄之前，您應該使用 GetVolumeInformation 函式來判斷檔案系統的功能。
ms.assetid: 008e0cc4-bc12-47e8-a8b7-d4fa9395fceb
title: 取得磁片區資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc5323c3f82db1115a81902f156e9366abad31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512024"
---
# <a name="obtaining-volume-information"></a>取得磁片區資訊

[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)函式會取得指定磁片區上檔案系統的相關資訊。 這項資訊包括磁片區名稱、磁片區序號、檔案系統名稱、檔案系統旗標、檔案名的最大長度等等。 存取指定磁片區上的檔案和目錄之前，您應該使用 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式來判斷檔案系統的功能。 此函式會傳回值，您可以使用這些值來調整應用程式，以有效地與檔案系統搭配使用。

一般而言，您應該避免使用靜態緩衝區作為檔案名和路徑。 相反地，請使用 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 傳回的值，以在需要時配置緩衝區。 如果您必須使用靜態緩衝區，請保留256個字元的檔案名和260個字元的路徑。

[**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)和 [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)函式會分別取出系統目錄和 Windows 目錄的路徑。

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)函式會抓取有關磁片區的組織資訊，包括每個磁區的位元組數目、每個叢集的磁區數目、可用叢集的數目，以及叢集總數。 不過， **GetDiskFreeSpace** 無法報告大於 2 GB 的磁片區大小。 若要確保您的應用程式能與大型容量硬碟搭配運作，請使用 [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) 函式。

[**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea)函式會指出指定的磁碟機號所參照的磁片區是卸載式、固定、CD-ROM、RAM 或網路磁碟機機。

[**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives)函式會識別目前的磁片區。 [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)函式會針對存在的每個磁片區，抓取以 null 終止的字串。 當需要根目錄時，請使用這些字串。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案系統識別](file-system-recognition.md)
</dt> </dl>

 

 
