---
description: Tablet PC InkPicture 控制項的參考主題。
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: InkPicture 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985059"
---
# <a name="inkpicture-control"></a>InkPicture 控制項

[InkPicture](inkpicture-control-reference.md)控制項可讓您將影像 ( .jpg、.bmp、.png 或 .gif 格式) 在使用者可以加入筆墨的應用程式中。 它適用于不需要將筆墨辨識為文字，但會儲存為筆墨的情況。

使用者使用畫筆將筆墨新增至透明層。 使用者可以重新調整 [InkPicture](inkpicture-control-reference.md) 視窗的大小，而不會遺失任何筆墨資訊，即使在調整大小的情況下裁剪筆墨也一樣。

[InkPicture](inkpicture-control-reference.md)控制項包含基本列印支援;不過，您可以自行執行預覽列印或其他先進的列印功能。

Managed ( .NET Framework [InkPicture](/previous-versions/ms583740(v=vs.100)) 的) 執行會繼承 [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) 類別。

依預設，如果不在高對比模式中，則筆墨會著色為黑色;否則，它會設定為目前的系統色彩設定 (色彩 \_ WINDOWTEXT) 值。 此外，根據預設， [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) 是 **FALSE**。

在 [InkPicture](inkpicture-control-reference.md) 控制項中，使用 [**筆墨**](inkdisp-class.md) 物件來載入及儲存筆跡。

> [!Note]  
> 當您將 [**system.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) 設定為 [ **刪除** ] 或 [ **選取**] 時，就會觸發其他事件 (例如 [**筆觸**](inkpicture-stroke.md) 事件) 。 如果您想要執行自己的刪除或選取模式，這些事件會很有用。

 

如需 [InkPicture](inkpicture-control-reference.md) 控制項的詳細參考資訊，請參閱 InkPicture。

下列各節詳細說明 [InkPicture](inkpicture-control-reference.md) 控制項的使用：

-   [使用圖片](working-with-pictures.md)
-   [在舊版 Windows 上使用 InkPicture](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
