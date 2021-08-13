---
description: 若要取得壓縮的檔案大小，請使用 GetCompressedFileSize 函數。
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: 取得壓縮檔案的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3090272145c19ec5040a8df573a5100cad4d21b3fdc6f543e40d24f933dc3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648563"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a>取得壓縮檔案的大小

您可以使用 [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) 函式來取得檔案的壓縮大小。 如果檔案已壓縮，壓縮的大小將會小於其未壓縮的大小。 您可以使用 [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) 函數來判斷檔案的未壓縮大小。

 

 



