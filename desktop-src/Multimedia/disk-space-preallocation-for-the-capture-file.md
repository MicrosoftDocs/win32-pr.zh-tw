---
title: Capture 檔案的磁碟空間預先配置
description: Capture 檔案的磁碟空間預先配置
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE 訊息
- capFileAlloc 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300692"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Capture 檔案的磁碟空間預先配置

預先配置磁碟空間可供 capture 檔案在開始進行捕獲作業之前，先在磁片上建立指定大小的檔案。 預先配置 capture 檔案可減少在進行 capture 時所需的處理，並導致減少捨棄的畫面格。 您可以使用 [ [**WM \_ CAP 檔案 \_ \_ 配置**](wm-cap-file-allocate.md) 訊息 (] 或 [ [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) 宏) 來預先配置 capture 檔。

一般而言，您的應用程式應預先配置足夠的磁碟空間，以包含預期的最大 capture 檔。 預先配置磁碟空間不會限制所捕獲檔案的大小。 如果捕捉的資料超過配置的空間，則會自動放大檔案大小。 對 capture 檔案進行的後續寫入作業會重複使用配置給檔案的磁碟空間部分，以保留檔案的大小和片段。

您也可以藉由重組捕獲檔案來改善「捕獲效能」。 若要重組檔案，請使用磁碟重組工具，例如磁片磁碟重組工具。 如果您使用已重組的捕獲檔案，並于稍後將它放大，則應該重組放大的檔案。 擴大重組的捕獲檔案可將檔案的展開部分片段化，並降低捕捉作業的效能。

您也可以使用未壓縮的磁片來取得影片捕獲，以改善效能。 在 capture 期間壓縮資料可以限制磁片的捕獲輸送量。

應用程式可以保留永久的捕獲檔案，以避免每次啟動時預先配置和重組檔案所需的時間。 因為 capture 檔案可能需要相當大的磁碟空間，而且預先配置 capture 檔案會移除現有 capture 檔案中的所有資料，所以應用程式應該讓使用者決定檔案是永久或暫時性的。

 

 




