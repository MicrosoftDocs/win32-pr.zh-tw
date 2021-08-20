---
description: 應用程式可以使用 LZOpenFile、LZCopy 和 LZClose 函式，將多個檔案解壓縮。
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: 解壓縮多個檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e2d7aef19dc79d4ebc78c1b04bff77ffbbe0fc19ec68daec6d54fe7040e735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998028"
---
# <a name="decompressing-multiple-files"></a>解壓縮多個檔案

應用程式可以藉由執行下列工作來解壓縮多個檔案：

1.  藉由呼叫 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) 函數來開啟原始程式檔。
2.  藉由呼叫 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)來開啟目的地檔案。
3.  藉由呼叫 [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) 函式，將原始程式檔複製到目的地檔案。
4.  藉由呼叫 [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) 函數來關閉檔案。

 

 



