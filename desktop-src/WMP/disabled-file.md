---
title: 停用的檔案
description: 停用的檔案
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Windows Media Player行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 面板的美工檔案，已停用的檔案
- Windows Media Player行動面板，已停用的檔案
- 外觀，已停用的檔案
- 面板中已停用的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b7d7c052ed0de1a3e231bc204b87a84f1e9e10262acfe43df310d76f76577b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997351"
---
# <a name="disabled-file"></a>停用的檔案

停用的檔案包含當無法使用特定按鈕函式或關閉按鈕狀態時將顯示的影像。 例如，如果定義了空白的播放清單，則會顯示 [ **下一步]** 和 [ **上** 一個] 按鈕，而且應該使用停用的影像來顯示。 此外，針對切換按鈕，已停用的影像會用來指出狀態為 [關閉]。

下圖是一般停用的檔案。

![停用的檔案](images/cesdkdis.png)

這會儲存已停用的點擊類型按鈕影像。 影像類似于背景檔案，但色彩較淺。 使用在外觀定義檔案的點陣圖區段中定義的位移，按鈕影像會與背景檔案影像對齊。

請注意，按鈕影像的背景完全符合背景檔案中對應的區域。 這點很重要，因為當 [點擊類型] 按鈕無法使用時，為停用的影像定義的整個矩形將會取代背景檔案中的相符區域。 讓圖形保持與背景影像一致，以確保只有您想要顯示的按鈕部分會實際變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**美工檔案**](art-files-mobile.md)
</dt> </dl>

 

 




