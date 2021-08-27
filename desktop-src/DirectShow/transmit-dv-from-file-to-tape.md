---
description: 從檔案傳輸 DV 到磁帶
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: 從檔案傳輸 DV 到磁帶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bcd7bf716466cda2fc23a03968da4a51c005070f885183390f944d14994ec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086788"
---
# <a name="transmit-dv-from-file-to-tape"></a>從檔案傳輸 DV 到磁帶

從 DV AVI 檔傳輸到 VTR 磁帶有點複雜，因為檔案可以輸入-1 或類型2。 若要將 DV 檔案傳送至磁帶，請執行下列動作：

1.  建立 [MSDV 驅動程式](msdv-driver.md) 篩選器的實例。 如需詳細資訊，請參閱 [選取擷取裝置](selecting-a-capture-device.md)。
2.  請確定裝置處於 VTR 模式。 否則，您無法傳輸至磁帶。請參閱 [裝置模式](device-mode.md)。
3.  如[《 capture Graph builder](about-the-capture-graph-builder.md)》中所述，初始化 capture Graph builder。
4.  建立圖形。 圖形設定取決於 DV 檔案類型：
    -   [從類型1檔案傳輸](transmit-from-type-1-file.md)
    -   [從類型2檔案傳輸](transmit-from-type-2-file.md)
5.  將裝置進入記錄暫停模式，如 [控制 DV](controlling-a-dv-camcorder.md)攝影機所述。
6.  暫停篩選圖形。 當篩選圖形暫停時，它會傳送連續的資料流程，以重複第一個畫面格。
7.  若要開始傳輸，請將裝置放入記錄模式，然後執行篩選圖形。 它會將裝置設為一定的時間，直到記錄標頭能夠錄製為止，因此請等候大約兩秒，然後再執行圖形。 這可能會導致磁帶的開頭有幾個重複的畫面格，但它可確保不會遺失任何資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 



