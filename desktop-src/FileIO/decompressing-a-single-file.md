---
description: 應用程式可以使用 LZOpenFile、LZCopy 和 LZClose 函式來解壓縮單一壓縮檔案。
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: 解壓縮單一檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8da6ee4ee80e42d6ff70c3d9c50efdc572f97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969290"
---
# <a name="decompressing-a-single-file"></a>解壓縮單一檔案

應用程式可以執行下列工作，以解壓縮單一壓縮檔案：

1.  藉由呼叫 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) 函數來開啟原始程式檔。
2.  藉由呼叫 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)來開啟目的地檔案。
3.  藉由呼叫 [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) 函式並傳遞 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)所傳回的控制碼，將原始程式檔複製到目的地檔案。
4.  藉由呼叫 [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) 函數來關閉檔案。

 

 



