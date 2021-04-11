---
description: AreFileApisANSI 函式會判斷檔案 i/o 函數是否使用 ANSI 或 OEM 字元集字碼頁。
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: 判斷目前的字元集字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849504"
---
# <a name="determining-the-current-character-set-code-page"></a>判斷目前的字元集字碼頁

[**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi)函式會判斷檔案 i/o 函數是否使用 ANSI 或 OEM 字元集字碼頁。 [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi)函式會讓函數使用 ANSI 字碼頁。 [**可透過 setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem)函式會讓函數使用 OEM 字碼頁。

依預設，檔案 i/o 函數會使用 ANSI 檔案名。 接受或傳回檔案名的 Kernel32.dll 所匯出的函式會受到檔案字碼頁設定的影響。

[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi)和 [**可透過 setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem)都會設定每個進程的字碼頁，而不是每個執行緒或每部電腦的字碼頁。

 

 



