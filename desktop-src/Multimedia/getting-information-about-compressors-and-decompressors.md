---
title: 取得壓縮機和 Decompressors 的相關資訊
description: 取得壓縮機和 Decompressors 的相關資訊
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，取得有關壓縮機的資訊
- BC-VCM-LVM-HYPERV (video 壓縮管理員) ，取得有關壓縮機的資訊
- ICGetInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b6acacd97b514edcf0328a8127f97152554015694eba3f8e5bf3b76214de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678609"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>取得壓縮機和 Decompressors 的相關資訊

若要取得有關壓縮程式或解壓縮程式的一般資訊，您的應用程式可以使用 [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) 函數。 此函式會填入 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) 結構，其中包含有關壓縮程式或解壓縮程式的資訊。 您的應用程式必須配置 **ICINFO** 結構的記憶體，並在 **ICGetInfo** 中將指標傳遞給它。 除非您的應用程式會搜尋特定的壓縮程式或解壓縮程式，否則 **ICINFO** 結構中的旗標會提供有關壓縮程式或解壓縮程式功能的最有用資訊。

若要取得壓縮程式或解壓縮程式的預設索引鍵畫面播放速率和預設品質值，您的應用程式可以傳送 [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md)和 [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md)訊息 (或使用 [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate)和 [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality)宏) 。

若要判斷壓縮程式或解壓縮程式的最佳顯示格式，您的應用程式可以使用 [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) 函數。

若要判斷壓縮程式或解壓縮程式是否可以顯示 [about （關於）] 對話方塊，請將訊息的 [**\_ 相關 ICM**](icm-about.md)傳送 (或使用 [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout)宏) 。 您也可以藉由傳送 ICM 的 \_ 訊息，並將 *wParam* 參數的值變更 (或使用 [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout)宏) ，來顯示壓縮程式或解壓縮程式的 [關於] 對話方塊。

 

 




