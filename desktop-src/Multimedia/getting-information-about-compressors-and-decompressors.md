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
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932259"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>取得壓縮機和 Decompressors 的相關資訊

若要取得有關壓縮程式或解壓縮程式的一般資訊，您的應用程式可以使用 [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) 函數。 此函式會填入 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) 結構，其中包含有關壓縮程式或解壓縮程式的資訊。 您的應用程式必須配置 **ICINFO** 結構的記憶體，並在 **ICGetInfo** 中將指標傳遞給它。 除非您的應用程式會搜尋特定的壓縮程式或解壓縮程式，否則 **ICINFO** 結構中的旗標會提供有關壓縮程式或解壓縮程式功能的最有用資訊。

若要取得預設的金鑰畫面播放速率和壓縮程式或解壓縮程式的預設品質值，您的應用程式可以傳送 [**icm \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) 和 [**icm \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) 訊息 (或使用 [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) 和 [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) 宏) 。

若要判斷壓縮程式或解壓縮程式的最佳顯示格式，您的應用程式可以使用 [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) 函數。

若要判斷壓縮程式或解壓縮程式是否可以顯示 [關於] 對話方塊，請傳送訊息 (的 [**ICM \_**](icm-about.md) ，或使用 [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) 宏) 。 您也可以藉由傳送 \_ 關於訊息的 ICM、變更 *wParam* 參數的值 (或使用 [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) 宏) ，來顯示壓縮程式或解壓縮程式的 [關於] 對話方塊。

 

 




