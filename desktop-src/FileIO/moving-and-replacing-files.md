---
description: 使用 CopyFileEx、CreateFile、Replacefile 和 MoveFileEx 函數移動和取代檔案的考慮。
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: 移動和取代檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c78085865006d1dfbbe322239c4704d215d038897b81d1f139d66d06f65bbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696008"
---
# <a name="moving-and-replacing-files"></a>移動和取代檔案

在可以執行複製作業之前，必須先關閉或開啟來源檔案以進行讀取。 沒有任何執行緒可以開啟來源檔案進行寫入。 若要將現有的檔案複製到新的檔案，請使用 [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) 或 [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) 函數。 如果目的地檔案已經存在，應用程式可以指定 **CopyFile** 和 **CopyFileEx** 是否失敗。 如果目的地檔案存在且為開啟狀態，則必須已使用適用的共用許可權開啟該檔案。 如需詳細資訊，請參閱 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)。

[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)函式也可讓應用程式指定回呼函式的位址 (請參閱 [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)) ，每次複製檔案的另一個部分時，就會呼叫此函式。 應用程式可以使用這項資訊來顯示指標，顯示覆制的總位元組數（以總檔案大小的百分比表示）。

[**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)函式會以另一個檔案取代一個檔案，選項是建立原始檔案的備份副本。 函式會保留原始檔案的屬性，例如其建立時間、Acl 和加密屬性。

您也必須先關閉檔案，應用程式才能將它移動。 [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)和 [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)函式會將現有的檔案複製到新位置，並刪除原始的檔案。

[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)函式也允許應用程式指定移動檔案的方式。 此函數可以取代現有的檔案、跨磁片區移動檔案，以及延遲移動檔案，直到作業系統重新開機為止。

 

 



