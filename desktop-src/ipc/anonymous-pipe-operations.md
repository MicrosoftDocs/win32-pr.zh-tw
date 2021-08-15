---
description: 匿名管道作業，包括管道建立、寫入管道、管道控制碼。
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: 匿名管道作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4c684daab5dd1c18dbf5eb22e2191f193e7ecc3b088ac58e3f680f442897a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350708"
---
# <a name="anonymous-pipe-operations"></a>匿名管道作業

[**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)函式會建立匿名管道，並傳回兩個控制碼：管道的讀取控制碼和管道的寫入控制碼。 讀取控制碼具有管道的唯讀存取權，且寫入控制碼具有管道的僅限寫入存取權。 若要使用管道進行通訊，管道伺服器必須將管道控制碼傳遞至另一個進程。 這通常是透過繼承來完成;也就是說，進程允許子進程繼承控制碼。 此程式也可以使用 [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) 函式來複製管道控制碼，並使用某種形式的處理序間通訊（例如 DDE 或共用記憶體）將它傳送至不相關的進程。

管道伺服器可以將讀取控制碼或寫入控制碼傳送到管道用戶端，視用戶端是否應該使用匿名管道來傳送資訊或接收資訊而定。 若要從管道讀取，請在 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 函式的呼叫中使用管道的讀取控制碼。 當另一個進程寫入管道時， **ReadFile** 呼叫會傳回。 如果已關閉管道的所有寫入控制碼，或在完成讀取作業之前發生錯誤，則 **ReadFile** 呼叫也會傳回。

若要寫入管道，請在 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函式的呼叫中使用管道的寫入控制碼。 **WriteFile** 呼叫必須等到將指定的位元組數目寫入管道或發生錯誤之後，才會傳回。 如果管道緩衝區已滿，且要寫入的位元組數較多，則在另一個進程從管道讀取時， **WriteFile** 不會傳回，因此可提供更多的緩衝區空間。 當管道伺服器呼叫 [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)時，會指定該管道的緩衝區大小。

匿名管道不支援非同步 (重迭) 讀取和寫入作業。 這表示您不能使用 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) 函數搭配匿名管道。 此外，當搭配匿名管道使用這些函式時，會忽略 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)和 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)的 *lpOverlapped* 參數。

匿名管道會一直存在，直到所有管道控制碼（讀取和寫入）都已關閉為止。 進程可以使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式來關閉其管道控制碼。 進程終止時，所有管道控制碼也會關閉。

匿名管道會使用具有唯一名稱的具名管道來執行。 因此，您通常可以將控制碼傳遞至需要具名管道控制碼的函式。

 

 
