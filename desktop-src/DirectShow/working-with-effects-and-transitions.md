---
description: 使用效果和轉換
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: 使用效果和轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945432"
---
# <a name="working-with-effects-and-transitions"></a>使用效果和轉換

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

效果會修改單一剪輯、追蹤或組合。 轉換會從一個曲目建立 seques，或 compositionsto 另一個。

[DirectShow 編輯服務](directshow-editing-services.md) 會使用 DirectX 轉換物件來進行影片轉換和影片效果。 針對影片轉換，請使用任何2D 雙輸入 DirectX 轉換物件。 針對影片效果，請使用任何2-d 的單一輸入 DirectX 轉換物件。 Microsoft 不再支援協力廠商 DirectX 轉換物件的開發。 但是，有數個會隨 DirectShow 提供，有些則是由 Microsoft Internet Explorer 提供。 如需 Internet Explorer 所提供之轉換的詳細資訊，請參閱 [視覺化篩選和轉換參考](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85))。

針對音訊效果，您可以使用任何 DirectShow 音訊效果篩選。 DES 也會提供 [音量信封效果](volume-envelope-effect.md) ，以在播放軌或剪輯上設定音量。 DES 不支援音訊轉換。

本節包含下列主題：

-   [新增效果和轉換物件](adding-effect-and-transition-objects.md)
-   [預覽效果和轉換](previewing-effects-and-transitions.md)
-   [列舉效果和轉換](enumerating-effects-and-transitions.md)
-   [設定效果和轉換的屬性](setting-properties-on-effects-and-transitions.md)
-   [轉換方向](transition-direction.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務](using-directshow-editing-services.md)
</dt> </dl>

 

 
