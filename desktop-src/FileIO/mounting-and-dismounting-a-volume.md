---
description: 建立裝載的資料夾是兩個步驟的程式。
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: 建立載入的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3067af38a893085adcc407263711c80a64c3eea1e535f6814db2cd2742f899
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650228"
---
# <a name="creating-mounted-folders"></a>建立載入的資料夾

建立裝載的資料夾是兩個步驟的程式。 首先，使用掛接點來呼叫 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) ， (磁碟機號、磁片區 GUID 路徑，或要指派給掛接資料夾之磁片區的已掛接資料夾) 。 然後使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式，將傳回的磁片區 GUID 路徑與另一個磁片區上所需的目錄產生關聯。 如需範例程式碼，請參閱 [建立載入的資料夾](mounting-a-volume-at-a-mount-point.md)。

您的應用程式可以指定磁片區上的任何空白目錄，而非根節點做為裝載的資料夾。 當您呼叫 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式時，該目錄會成為裝載的資料夾。 您可以將相同的磁片區指派給多個裝載的資料夾。

建立掛接的資料夾之後，它會透過電腦自動重新開機進行維護。

如果磁片區失敗，任何已指派給該磁片區上掛接之資料夾的磁片區，都無法再透過這些掛接的資料夾存取。 例如，假設您有兩個磁片區： C：和 D：，而該 D：與裝載的資料夾 C： MountD 相關聯 \\ \\ 。 如果磁片區 C：失敗，則無法再透過路徑 C： MountD 存取磁片區 D \\ ： \\ 。

只有 NTFS 檔案系統磁片區可以有掛接的資料夾，但裝載資料夾的目標磁片區可以是非 NTFS 磁片區。

裝載的資料夾是使用重新分析點來執行，並受限於其限制。 如需詳細資訊，請參閱重新 [分析點](reparse-points.md)。 不需要操作重新分析點來使用掛接的資料夾; [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 等函數會為您處理所有的重新分析點詳細資料。

因為掛接的資料夾是目錄，您可以重新命名、移除、移動和操作它們，就像其他目錄一樣。

 (附注： TechNet 檔會使用一詞掛接的 *磁片磁碟機* 來參考 *裝載的資料夾*。 ) 

 

 



