---
description: 強制插入主要畫面格
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: '強制插入主要畫面格 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468624"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>強制插入主要畫面格 (Microsoft 媒體基礎) 

當您設定影片編碼器物件時，可以在編碼內容中設定主要畫面格的最大間隔。 不過，編解碼器會將主要畫面格放在該間隔內，如內容所規定;主要畫面格間隔不是常數。 對於某些應用程式而言，主要畫面格距離相當重要。 例如，影片編輯應用程式需要主要畫面格位於編輯器的邏輯位置，例如場景中斷和拍攝轉換。

強制插入主要畫面格是一項功能，可讓您要求輸入框架以主要畫面格的形式編碼。 編碼器會嘗試接受這些要求，但針對編碼會話設定的緩衝區設定 (位元速率和緩衝區視窗) 一律優先。

影片編碼器物件會執行強制的主要畫面格插入，以回應附加至輸入範例的資料單位延伸模組。 如需有關資料單位延伸的詳細資訊，請參閱 [使用資料單位延伸](usingdataunitextensions.md)。

強制主要畫面格插入的延伸模組資料是以下列 GUID 值來識別： **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**。 個別的延伸模組為 **BOOL** 值。 將值設定為 **TRUE** ，表示主要畫面格要求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用資料單位延伸模組](usingdataunitextensions.md)
</dt> <dt>

[使用影片](workingwithvideo.md)
</dt> </dl>

 

 



