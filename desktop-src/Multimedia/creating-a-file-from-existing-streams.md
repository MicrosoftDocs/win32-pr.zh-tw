---
title: 從現有的資料流程建立檔案
description: 從現有的資料流程建立檔案
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- AVISave 函式
- AVISaveV 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15a6ad3770f93bc2fb77dcb79975e1e9aa1fc8da7319e34c140baf488a69554
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498008"
---
# <a name="creating-a-file-from-existing-streams"></a>從現有的資料流程建立檔案

建立包含資料流程之檔案的其中一種方式，是將現有的資料流程合併成新的檔案。 提供新檔案之資料的資料流程可以位於記憶體或一或多個檔案中。

您可以使用 [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) 函數，從數個數據流建立檔案。 此函式會建立檔案，並將其呼叫順序中指定的資料流程寫入檔案。 **AVISave** 的呼叫序列會使用引數數目的引數，這些引數包含在新檔案中結合之資料流程的介面。

您也可以使用 [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) 函式，將資料流程合併在新的檔案中。 此函式提供與 **AVISave** 相同的功能，但是當您使用 **AVISaveV** 時，您的應用程式會將資料流程指定為數組，而不是變數數目的引數。

您可以建立一個對話方塊，讓使用者可以使用 [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) 函數來選取新檔案的壓縮設定。 對話方塊會顯示目前的壓縮設定，並讓使用者編輯這些設定。 壓縮設定變更會儲存在 [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) 結構中。

您也可以加入具有 [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) 和 [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) 的回呼函式，讓您的應用程式用來顯示寫入檔案的進度，如有需要，可讓使用者取消儲存作業。 您可以在 **AVISave** 或 **AVISaveV** 的呼叫順序中包含回呼函式的位址。

您可以讓使用者使用 [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) 函式來選取新檔案的檔案名。 此函式會顯示 [另存新檔] 對話方塊，讓使用者可以在其中預覽 AVI 檔案的影片資料流程) 的第一個串流 (。

您可以使用 [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) 函式來建立檔案介面指標 (以及一組資料流程的虛擬檔案) 。 其他 AVIFile 函式可以使用此函式所傳回的檔案介面指標，來存取虛擬檔案中的資料流程。 當您使用完虛擬檔案之後，請使用 [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) 函數來刪除檔案介面指標。

> [!Note]  
> 若要將影像和音訊效能降至最低，請避免壓縮 AVI 檔案一次以上。 在編輯系統中結合未壓縮的部分影片，然後壓縮最終產品。 如需壓縮選項的詳細資訊，請參閱 [影片壓縮管理員](video-compression-manager.md)。

 

 

 




