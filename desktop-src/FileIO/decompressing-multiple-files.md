---
description: 應用程式可以使用 LZOpenFile、LZCopy 和 LZClose 函式，將多個檔案解壓縮。
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: 解壓縮多個檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992018"
---
# <a name="decompressing-multiple-files"></a>解壓縮多個檔案

應用程式可以藉由執行下列工作來解壓縮多個檔案：

1.  藉由呼叫 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) 函數來開啟原始程式檔。
2.  藉由呼叫 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)來開啟目的地檔案。
3.  藉由呼叫 [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) 函式，將原始程式檔複製到目的地檔案。
4.  藉由呼叫 [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) 函數來關閉檔案。

 

 



