---
description: 標籤是指派給磁片區（通常是由使用者使用）的易記名稱，可讓您更容易辨識。 磁片區可以有標籤、磁碟機號、兩者或兩者皆有。 若要設定磁片區的標籤，請使用 SetVolumeLabel 函數。
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: 命名磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6435b6b5c7283cf2fb9a98951698f79646dfdffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851199"
---
# <a name="naming-a-volume"></a>命名磁片區

標籤是指派給磁片區（通常是由使用者使用）的易記名稱，可讓您更容易辨識。 磁片區可以有標籤、磁碟機號、兩者或兩者皆有。 若要設定磁片區的標籤，請使用 [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) 函數。

有幾個因素可能會讓您難以使用磁碟機號和標籤來識別特定磁片區。 其中一個是磁片區不需要有磁碟機號或標籤。 另一種方式是讓兩個不同的磁片區有相同的標籤，而不是由磁碟機號區別。 第三個因素是在電腦上新增和移除磁片區時，可以變更磁碟機號指派。

為了解決這個問題，作業系統使用磁片區 *GUID 路徑* 來識別磁片區。 以下是這種形式的字串：

"\\\\?\\Volume {*GUID*} \\ "

其中 *guid* 是識別磁片區 (guid) 的全域唯一識別碼。

磁片區 GUID 路徑有時稱為 *唯一磁片區名稱*，因為磁片區 guid 路徑只能參考一個磁片區。 不過，因為磁片區可以有一個以上的磁片區 GUID 路徑，所以此詞彙很誤導。

" \\ \\ ？ \\ " 前置詞會停用路徑剖析，而不會被視為路徑的一部分。 如需 "？" 前置詞的詳細資訊 \\ \\ \\ ，請參閱[命名檔案或目錄](naming-a-file.md)。

使用具有 " \\ \\ ？" 前置詞的磁片區 GUID 路徑時，您必須指定完整路徑 \\ 。

*裝載的資料夾* 是一個磁片區上的資料夾與另一個磁片區之間的關聯，因此可以使用資料夾路徑來存取磁片區。 例如，如果您使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式來建立將磁片區 "d： \\ " 與資料夾 "C： MountD" 產生關聯的已掛接資料夾 \\ \\ ，則可以使用任一路徑 ( "d： \\ " 或 "C： \\ MountD \\ " ) 來存取磁片區 "d： \\ "。

*磁片區掛接點* 是可用於存取磁片區的任何使用者模式路徑。 磁片區掛接點有三種類型：

-   磁碟機號，例如 "C： \\ "。
-   磁片區 GUID 路徑，例如 " \\ \\ ？ \\磁片區 {26a21bda-a627-11d7-9931-806e6f6e6963} \\ "。
-   裝載的資料夾，例如 "C： \\ MountD \\ "。

將磁片區 GUID 路徑當作輸入參數的所有磁片區和已掛接的資料夾函式都需要尾端的反斜線。 所有會傳回磁片區 GUID 路徑的磁片區和已掛接資料夾函式都會提供尾端的反斜線，但 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式並不會發生這種情況。 您可以藉由呼叫 **CreateFile** 來開啟磁片區，並從您指定的磁片區名稱中省略尾端的反斜線。 **CreateFile** 會以附加的反斜線做為磁片區的根目錄，來處理磁片區 GUID 路徑。

當第一次安裝磁片區以及格式化磁片區時，作業系統會將磁片區 GUID 路徑指派給磁片區。 磁片區和裝載的資料夾功能會使用磁片區 GUID 路徑來存取磁片區。 若要取得磁片區的磁片區 GUID 路徑，請使用 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) 函數。

建立掛接的資料夾時，路徑長度可能會是個問題，其會將具有深度目錄樹狀目錄的磁片區與另一個磁片區上的目錄產生關聯。 這是因為磁片區的路徑會串連至目錄的路徑。 全域定義的常數 **最大 \_ 路徑** 會定義路徑可具有的最大字元數。  (如需 **最大 \_ 路徑** 的詳細資訊，請參閱 [命名檔案或目錄](naming-a-file.md)。 ) 您可以執行下列其中一項動作來避免這個限制：

-   請依磁片區 GUID 路徑來參考磁片區。
-   使用 Unicode (W) 檔案函式版本，其支援 \\ \\ ？前置詞 \\ 。

 

 



