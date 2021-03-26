---
title: Memory-Mapped 檔案資訊
description: 記憶體對應檔 (或檔案對應) 是將檔案的內容與進程的部分虛擬位址空間產生關聯的結果。 可以用來在兩個或多個進程之間共用檔案或記憶體。
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093120"
---
# <a name="memory-mapped-file-information"></a>Memory-Mapped 檔案資訊

*記憶體對應* 檔 (或檔案 *對應*) 是將檔案的內容與進程的部分虛擬位址空間產生關聯的結果。 可以用來在兩個或多個進程之間共用檔案或記憶體。

[**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea)函式會接收進程控制碼和位址的指標做為輸入。 如果位址是在進程的虛擬位址空間中的記憶體對應檔案內，則函式會傳回記憶體對應檔的名稱。 **GetMappedFileName** 所傳回的檔案名會使用裝置表單，而不是磁碟機號。 例如，檔案名 c： \\ winnt \\ system32 \\ ctype. nls 在裝置形式中看起來會像這樣：

\\裝置 \\ Harddisk0 \\ Partition1 \\ WINNT \\ System32 \\ ctype. nls

如需記憶體對應檔案的詳細資訊，請參閱檔案 [對應](/windows/desktop/Memory/file-mapping)。 如需將裝置形式的檔案名轉換成磁碟機號的範例，請參閱 [從檔案控制代碼取得檔案名](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle)。

 

 