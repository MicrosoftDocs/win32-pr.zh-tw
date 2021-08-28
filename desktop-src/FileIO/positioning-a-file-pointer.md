---
description: Windows 使用檔案指標來追蹤讀取或寫入的位元組。
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: 放置檔案指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93caefcb622f297d391aba4d695a2b0c2c2e2ca368a97c68332862a7f8bfa8a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951087"
---
# <a name="positioning-a-file-pointer"></a>放置檔案指標

當應用程式第一次呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)來開啟檔案時，Windows 會將檔案 [指標](file-pointers.md)放在檔案的開頭。 當位元組讀取或寫入檔案時，Windows 會將檔案指標前進到讀取或寫入的位元組數目。

應用程式可以藉由呼叫 [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)，將檔案指標定位至指定的位移。

[**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)函式也可以用來查詢目前的檔案指標位置，方法是指定檔案 **\_ 目前** 的移動方法和距離零的距離。

 

 



