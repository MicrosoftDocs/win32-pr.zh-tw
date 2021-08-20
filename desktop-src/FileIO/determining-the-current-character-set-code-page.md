---
description: AreFileApisANSI 函式會判斷檔案 i/o 函數是否使用 ANSI 或 OEM 字元集字碼頁。
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: 判斷目前的字元集字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18361c0553407ade59c2d1de61ac2fb20d18d5b9d46018bcbc74dc3a114917b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150655"
---
# <a name="determining-the-current-character-set-code-page"></a>判斷目前的字元集字碼頁

[**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi)函式會判斷檔案 i/o 函數是否使用 ANSI 或 OEM 字元集字碼頁。 [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi)函式會讓函數使用 ANSI 字碼頁。 [**可透過 setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem)函式會讓函數使用 OEM 字碼頁。

依預設，檔案 i/o 函數會使用 ANSI 檔案名。 接受或傳回檔案名的 Kernel32.dll 所匯出的函式會受到檔案字碼頁設定的影響。

[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi)和 [**可透過 setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem)都會設定每個進程的字碼頁，而不是每個執行緒或每部電腦的字碼頁。

 

 



