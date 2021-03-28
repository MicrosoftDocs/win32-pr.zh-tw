---
description: 裝置相依點陣圖 (DDBs) 是使用單一結構（點陣圖結構）描述。
ms.assetid: 63ff9cd6-cd07-4085-b166-268e4d9b7aad
title: Device-Dependent 點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a3de2c59509c71b38f9981df330b3b28effa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114681"
---
# <a name="device-dependent-bitmaps"></a>Device-Dependent 點陣圖

裝置相依點陣圖 (DDBs) 是使用單一結構（ [**點陣圖**](/windows/win32/api/wingdi/ns-wingdi-bitmap) 結構）描述。 此結構的成員會指定矩形區域的寬度和高度（以圖元為單位）。將裝置選擇區中的專案對應到圖元的陣列寬度;和裝置的色彩格式，就色彩平面和每圖元的位數而言。 應用程式可以藉由呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式並指定適當的常數，來取得裝置的色彩格式。 請注意，DDB 不包含色彩值;相反地，色彩會採用裝置相依的格式。 如需詳細資訊，請參閱 [點陣圖中的色彩](color-in-bitmaps.md)。 因為每個裝置都可以有自己的一組色彩，所以針對某個裝置所建立的 DDB 可能無法在不同的裝置上正確顯示。

若要在裝置內容中使用 DDB，它必須具有該裝置內容的色彩組織。 因此，DDB 通常稱為 *相容的點陣圖* ，它的 GDI 效能通常會比 DIB 更好。 例如，若要建立視訊記憶體的點陣圖，最好使用具有與主顯示器相同色彩格式的相容點陣圖。 在視頻記憶體中，轉譯成點陣圖，並將它顯示在螢幕上，會比從系統記憶體表面或直接從 DIB 更快。

除了啟用更好的 GDI 效能，您也可以使用相容的點陣圖來捕捉影像 (請參閱 ) 抓取 [影像](capturing-an-image.md) ，並在執行時間為功能表建立點陣圖，請參閱 (的 [使用功能表](../menurc/using-menus.md) ) 中的「建立點陣圖」。

若要在具有不同色彩組織的裝置之間傳輸點陣圖，請使用 [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) 將相容的點陣圖轉換成 DIB，然後呼叫 [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) 或 [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) ，以將 DIB 顯示到第二個裝置。

有兩種類型的 DDBs： discardable 和 nondiscardable。 Discardable DDB 是一種點陣圖，如果點陣圖未選取到 DC，而且系統記憶體不足，系統就會捨棄該點陣圖。 [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)函式會建立 discardable 點陣圖。 [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)、 [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)和 [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)函數會建立 nondiscardable 點陣圖。

應用程式可以藉由初始化所需的結構並呼叫 [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) 函式，從 DIB 建立 DDB。 在 \_ **CreateDIBitmap** 的呼叫中指定 CBM INIT 相當於呼叫 [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) 函式以裝置的格式建立 DDB，然後呼叫 [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) 函式以將 DIB 位轉譯為 DDB。 若要判斷裝置是否支援 **SetDIBits** 函式，請呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式， \_ 並將 RC DI \_ 點陣圖指定為 RASTERCAPS 旗標。

 

 
