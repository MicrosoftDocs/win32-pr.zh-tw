---
description: 如何判斷指定的目錄是否為裝載的資料夾。
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: 判斷目錄是否為裝載的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851580"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>判斷目錄是否為裝載的資料夾

例如，當您使用僅限一個磁片區的備份或搜尋應用程式時，判斷目錄是否為掛接的資料夾會很有用。 如果您使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 之類的函式來為應用程式所限制的磁片區上的其他磁片區建立掛接的資料夾，則這類應用程式可以觸及多個磁片區的資訊。 如需詳細資訊，請參閱 [建立裝載的資料夾](mounting-and-dismounting-a-volume.md)。

若要判斷指定的目錄是否為裝載的資料夾，請先呼叫 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 函式，並檢查傳回值中的 **檔案屬性重新 \_ \_ 分析 \_ 點** 旗標，以查看目錄是否有相關聯的重新分析點。 如果有的話，請使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)和 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)函數來取得 [**WIN32 \_ FIND \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa)結構的 **dwReserved0** 成員中的重新分析標記。 若要判斷重新分析點是否為掛接的資料夾 (而不是其他形式的重新分析點) ，請測試標記值是否等於值 **IO 重新 \_ 分析 \_ 標記 \_ 裝入 \_ 點**。 如需詳細資訊，請參閱重新 [分析點](reparse-points.md)。

若要取得裝載資料夾的目標磁片區，請使用 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) 函式。

您可以使用類似的方式，藉由測試標記值是否為 **IO 重新 \_ 分析 \_ 標記 \_** 的符號連結，判斷重新分析點是否為符號連結。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案屬性常數**](file-attribute-constants.md)
</dt> </dl>

 

 



