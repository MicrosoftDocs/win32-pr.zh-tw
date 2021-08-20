---
title: 編輯資料流程
description: 編輯資料流程
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- CreateEditableStream 函式
- EditStreamCut 函式
- EditStreamCopy 函式
- EditStreamPaste 函式
- EditStreamClone 函式
- EditStreamSetInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8616b3560409dfd15991cbdb9c5c1ecd7492a11c3690ee3728b0e52ec8d0951a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988819"
---
# <a name="editing-streams"></a>編輯資料流程

您可以使用 [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) 函式來建立可編輯的資料流程。 此函式會初始化用來編輯資料流程的環境。 這包括建立新資料流程的介面，以及追蹤對資料流程所做之變更的內部編輯資料表。 **CreateEditableStream** 會將資料流程指標傳回給其他資料流程編輯函數所需的可編輯資料流程。 可編輯的資料流程指標也可供接受資料流程指標的其他 AVIFile 函式使用。

您可以使用 [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) 函數，從可編輯的資料流程中剪下一或多個範例。 若要從可編輯的資料流程移除範例，此函式會將專案加入至編輯資料表。 然後，此函式會在新的暫存資料流程中放置剪下範例的複本，而此資料流程的介面指標會在變數中傳回。

您可以使用 [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) 函式，將一個或多個範例從可編輯的資料流程複製到暫存資料流程。 **EditStreamCopy** 會將範例的複本放在新的暫存資料流程中，其介面指標會在變數中傳回。

您可以從資料流程複製一或多個範例，並使用 [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) 函式將它們貼到可編輯的資料流程中。 若要在指定的位置插入範例，此函式會在目標可編輯資料流程的編輯資料表中新增專案。

您可以使用 [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) 函數來複製可編輯的資料流程。 此函式會傳回新資料流程的資料流程介面指標。 您可以將這些資料流程複製到剪貼簿，或使用它們來維護對資料流程所做的編輯記錄。

您可以使用 [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) 函數來變更可編輯資料流程的數個特性。 此函式會更新優先權設定、語言、縮放和速率、開始時間、品質設定、目的地矩形維度和座標，以及資料流程的文字描述。 這些專案會儲存在與可編輯資料流程相關聯的 [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) 結構中。

您也可以使用 [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) 函數來變更可編輯資料流程的文字描述。 此函數會更新與可編輯資料流程相關聯之 **AVISTREAMINFO** 結構的 **>szname** 成員。

編輯函數可用於資料流程。 您必須個別剪下並貼上每個資料流程，然後使用 [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) 函式來建立新的檔案指標。

> [!Note]  
> 可編輯資料流程中的編輯資料表會維護資料流程的所有變更。 來來源資料流永遠不會變更。

 

 

 




