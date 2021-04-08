---
title: 使用具有 AVI 檔案的剪貼簿
description: 使用具有 AVI 檔案的剪貼簿
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- AVIPutFileOnClipboard 函式
- AVIGetFromClipboard 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673280"
---
# <a name="using-the-clipboard-with-avi-files"></a>使用具有 AVI 檔案的剪貼簿

剪貼簿可提供方便的暫存儲存體，讓應用程式用來複製或傳輸 AVI 檔案。 AVIFile 包含可用於磁片或記憶體檔案的剪貼簿函數。

您可以使用 [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) 函式，將檔案複製到剪貼簿。 若要將剪貼簿上的檔案寫入記憶體或磁片，請使用 [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) 函數。

您可以使用 [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) 函式清除剪貼簿中的檔案。 此函式不會清除剪貼簿中其他類型的資訊，例如文字。 如果您在應用程式中使用剪貼簿功能，請在關閉應用程式或關閉剪貼簿上的檔案之前，使用 **AVIClearClipboard** 清除剪貼簿。 無論是否已使用 **AVIPutFileOnClipboard** ，您都可以在應用程式中呼叫 **AVIClearClipboard** 。

> [!Note]  
> 如果您的應用程式將檔案複製到剪貼簿，而檔案中包含可能變更的資料流程資料，您可以使用 [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) 函式來建立複製資料流程的記憶體檔。 然後，您可以將檔案放在剪貼簿上，然後釋出原始檔案而不使它失效。

 

 

 




