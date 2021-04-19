---
description: MS-DOS 裝置名稱是指向 MS-DOS 裝置路徑的連接點。 這些連接會組成 MS-DOS 裝置命名空間。
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: 定義 MS-DOS 裝置名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed89e1d9938e320ecce3ff0b35b8ae0792fe219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993062"
---
# <a name="defining-an-ms-dos-device-name"></a>定義 MS-DOS 裝置名稱

MS-DOS 裝置名稱是指向 MS-DOS 裝置路徑的連接點。 這些連接會組成 MS-DOS 裝置命名空間。 呼叫 [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) 和 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函數來建立和修改這些連接。 [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) 會刪除 **SetVolumeMountPoint** 所建立的連接點，而 **DefineDosDevice** 會刪除它所建立的連接。

定義 MS-DOS 裝置名稱之後，所有進程都可以看到它。

-   所有 MS-DOS 裝置都會透過驗證識別碼以 Windows 識別。 驗證識別碼是在建立時，與每個登入會話相關聯的 LUID (本機唯一識別碼) 。
-   MS-DOS 裝置名稱的可見度會分類為全域或本機，並定義為包含在全域 MS-DOS 裝置和本機 MS-DOS 裝置命名空間中。 所有使用者都可以存取全域命名空間中的 MS-DOS 裝置內容，而且只有存取權杖包含與該本機 MS-DOS 裝置命名空間相關聯的 AuthenticationID，才能存取本機命名空間中的 MS-DOS 裝置內容。

多個本機 MS-DOS 裝置命名空間，一次只能存在於一部電腦上。

請注意，只有在 LocalSystem 內容中執行的處理常式可以呼叫 [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) ，以在全域 MS-DOS 裝置命名空間中建立 MS-DOS 裝置。 此外，當移除該 AuthenticationID 的最後一個參考時，會刪除對應至特定 AuthenticationID 的本機 MS-DOS 裝置命名空間。

當您的程式碼藉由呼叫 [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)來查詢現有的 ms-dos 裝置名稱時，它會先搜尋本機 MS-DOS 裝置命名空間。 如果在該處找不到，此函式就會搜尋全域 MS-DOS 裝置命名空間。 當您的程式碼透過此函式查詢所有現有的 MS-DOS 裝置名稱時，傳回的名稱清單取決於是否正在 LocalSystem 內容中執行。 如果是，則只會傳回全域 MS-DOS 裝置命名空間中包含的 MS-DOS 裝置名稱。 如果不是，將會傳回全域和本機 MS-DOS 裝置命名空間中的裝置名稱串連。 如果兩個命名空間都有裝置名稱， **QueryDosDevice** 會傳回本機 MS-DOS 裝置命名空間中的專案。 這也適用于 [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) 和 [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)傳回的所有 MS-DOS 裝置名稱清單。

請注意，可能會發生下列情況：

1.  使用者 A （未在 LocalSystem 內容中執行）會在對應的本機 MS-DOS 裝置命名空間中建立裝置名稱，且該裝置名稱不存在於全域 MS-DOS 裝置命名空間中。
2.  使用者 B 在 LocalSystem 內容中執行時，會在全域 MS-DOS 裝置命名空間中建立相同的裝置名稱。

在此案例中，使用者 A 將無法存取全域 MS-DOS 裝置命名空間中的裝置名稱，除非他或她移除或重新命名其本機 MS-DOS 裝置命名空間中的裝置名稱。 若要降低發生這種情況的可能性，您應該在全域 MS-DOS 裝置命名空間中配置 MS-DOS 磁碟機號（開頭為 C：），並以 Z:. 結尾。 此順序應該針對本機 MS-DOS 裝置命名空間中的 MS-DOS 磁碟機號配置進行反轉。

如果您不是在 LocalSystem 內容中執行， [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) 將不允許您在本機 MS-DOS 裝置命名空間中定義裝置名稱，如果該裝置名稱已存在於您的本機或全域 MS-DOS 裝置命名空間中。 呼叫 **DefineDosDevice** 之前，請先呼叫 [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) ，以判斷您想要定義的裝置名稱是否存在於 MS-DOS 裝置命名空間中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[命名檔案、路徑和命名空間](naming-a-file.md)
</dt> </dl>

 

 



