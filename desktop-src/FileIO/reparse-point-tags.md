---
description: 每個重新分析點都有一個識別碼標記，如此您就可以有效率地區分不同類型的重新分析點，而不需要檢查重新分析點中的使用者定義資料。
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: 重新分析點標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b31d4a1765266295b85c95c0955ae9c51faeb34ae07f3af48288a17a50f2166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015186"
---
# <a name="reparse-point-tags"></a>重新分析點標記

每個重新分析點都有一個識別碼標記，如此您就可以有效率地區分不同類型的重新分析點，而不需要檢查重新分析點中的使用者定義資料。 系統會使用一組預先定義的標記，以及保留給 Microsoft 的標記範圍。 如果您在設定重新分析點時使用任何保留的標記，則作業會失敗。 未包含在這些範圍中的標記不會保留，而且可供您的應用程式使用。

當您設定重新分析點時，您必須標記要放置在重新分析點中的資料。 建立重新分析點之後，如果新資料的標記不符合現有資料的標記，新的設定作業就會失敗。 如果標記相符，則設定作業會覆寫現有的重新分析點。

若要取出重新分析點標記，請使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) 函數。 如果 **dwFileAttributes** 成員包含 **檔案屬性重新 \_ \_ 分析 \_ 點** 屬性，則 **dwReserved0** 成員會指定重新分析點。

## <a name="tag-contents"></a>標記內容

重新分析標記會儲存為 **DWORD** 值。 Bits 會定義某些屬性，如下圖所示。

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

低16位會決定重新分析點的種類。 高16位具有保留給未來使用的12個位，以及代表標記的特定屬性和重新分析點所代表之資料的4個位。 下表描述這些位。



| bit | 描述                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Microsoft 位。 如果設定此位，則標記是由 Microsoft 所擁有。 所有其他標記都必須使用零來表示此位。 |
| R   | 保護所有非 Microsoft 標記都必須是零。                                                           |
| N   | 名稱代理位。 如果設定此位，則檔案或目錄代表系統中的另一個命名實體。 |



 

下列宏有助測試標記：

-   [**IsReparseTagMicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**IsReparseTagNameSurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

如果已設定相關聯的位，每個宏都會傳回非零值。

以下是 Microsoft 預先定義的重新分析標記值;它們定義于 WinNT 中：

-   **IO_REPARSE_TAG_AF_UNIX**
-   **IO_REPARSE_TAG_APPEXECLINK**
-   **IO_REPARSE_TAG_CLOUD**
-   **IO_REPARSE_TAG_CLOUD_1**
-   **IO_REPARSE_TAG_CLOUD_2**
-   **IO_REPARSE_TAG_CLOUD_3**
-   **IO_REPARSE_TAG_CLOUD_4**
-   **IO_REPARSE_TAG_CLOUD_5**
-   **IO_REPARSE_TAG_CLOUD_6**
-   **IO_REPARSE_TAG_CLOUD_7**
-   **IO_REPARSE_TAG_CLOUD_8**
-   **IO_REPARSE_TAG_CLOUD_9**
-   **IO_REPARSE_TAG_CLOUD_A**
-   **IO_REPARSE_TAG_CLOUD_B**
-   **IO_REPARSE_TAG_CLOUD_C**
-   **IO_REPARSE_TAG_CLOUD_D**
-   **IO_REPARSE_TAG_CLOUD_E**
-   **IO_REPARSE_TAG_CLOUD_F**
-   **IO_REPARSE_TAG_CLOUD_MASK**
-   **IO_REPARSE_TAG_CSV**
-   **IO_REPARSE_TAG_DEDUP**
-   **IO_REPARSE_TAG_DFS**
-   **IO_REPARSE_TAG_DFSR**
-   **IO_REPARSE_TAG_FILE_PLACEHOLDER**
-   **IO_REPARSE_TAG_GLOBAL_REPARSE**
-   **IO_REPARSE_TAG_HSM**
-   **IO_REPARSE_TAG_HSM2**
-   **IO_REPARSE_TAG_MOUNT_POINT**
-   **IO_REPARSE_TAG_NFS**
-   **IO_REPARSE_TAG_ONEDRIVE**
-   **IO_REPARSE_TAG_PROJFS**
-   **IO_REPARSE_TAG_PROJFS_TOMBSTONE**
-   **IO_REPARSE_TAG_SIS**
-   **IO_REPARSE_TAG_STORAGE_SYNC**
-   **IO_REPARSE_TAG_SYMLINK**
-   **IO_REPARSE_TAG_UNHANDLED**
-   **IO_REPARSE_TAG_WCI**
-   **IO_REPARSE_TAG_WCI_1**
-   **IO_REPARSE_TAG_WCI_LINK**
-   **IO_REPARSE_TAG_WCI_LINK_1**
-   **IO_REPARSE_TAG_WCI_TOMBSTONE**
-   **IO_REPARSE_TAG_WIM**
-   **IO_REPARSE_TAG_WOF**

為了確保標記的唯一性，Microsoft 提供了散發新標記的機制。 如需詳細資訊，請參閱可 [安裝的檔案系統 (IFS) 套件](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx)。

 

 



