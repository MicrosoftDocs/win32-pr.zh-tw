---
description: 應用程式可以使用 FindFirstFile、FindFirstFileEx、FindNextFile 和 FindClose 函數，在目前的目錄中搜尋符合指定模式的所有檔案名。
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: 搜尋一個或多個檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972266"
---
# <a name="searching-for-one-or-more-files"></a>搜尋一個或多個檔案

應用程式可以使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)、 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)和 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數，在目前的目錄中搜尋符合指定模式的所有檔案名。 模式必須是有效的檔案名，而且可以包含萬用字元。

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)和 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)函式會建立 **FindFirstFileEx** 用來搜尋具有相同模式之其他檔案的控制碼。 所有函式都會傳回所找到檔案的相關資訊。 此資訊包含檔案名、大小、屬性和時間。

[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)函式也可讓應用程式根據其他搜尋準則來搜尋檔案。 此函式可以限制搜尋裝置名稱或目錄名稱。

[**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose)函式會終結 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)和 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)所建立的控制碼。

應用程式可以使用 [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) 函數，在特定路徑上搜尋單一檔案。

 

 
