---
title: DrawDib 作業
description: DrawDib 作業
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib，關於
- DrawDib，存取
- DrawDib，開啟
- DrawDib，作業
- 'DrawDib，裝置內容 (DC) '
- 'DC (裝置內容) '
- DrawDibOpen 函式
- DrawDibClose 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d331e2524c8b46c9e0781d1ff43a99b72a160a2b05acae7b853aabcbb9b8f0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941239"
---
# <a name="drawdib-operations"></a>DrawDib 作業

您可以使用 [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) 函數來存取整個 DrawDib 函數群組。 此函式會載入動態連結程式庫 (DLL) 、配置記憶體資源、建立 DrawDib 的裝置內容 (DC) ，以及維護已初始化之 Dc 數目的參考計數。 **DrawDibOpen** 也會傳回您搭配其他 DrawDib 函式使用之新 DC 的控制碼。

當您完成使用 [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) 函式時，可以釋放 DrawDib DC。 **DrawDibClose** 也會減少存取 DLL 之應用程式的參考計數。 對 **DrawDibClose** 的呼叫應該是您應用程式中的最後一個 DrawDib 函數。

您可以依需要建立任意數量的 DrawDib Dc。 您可以使用多個 DrawDib Dc 來同時繪製數個位圖。 您也可以建立多個 DrawDib Dc，各有獨特的特性，讓您的應用程式可以選擇，然後使用具有最適當設定的 DC。 例如，您可以在應用程式中建立兩個 DrawDib Dc：一個是以正常解析度顯示影像，另一個則顯示影像的放大部分。

若要有效率地執行，DrawDib 函式需要顯示介面卡及其驅動程式的相關資訊。 在第一次存取包含 DrawDib 函式的 DLL 時，會在顯示介面卡上執行一系列測試來取得顯示設定檔。 DrawDib 函式會將此資訊用於所有應用程式。 您可以使用 [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) 函式，視需要重複這些測試。

> [!Note]  
> 抓取和儲存顯示設定檔通常是一次出現。 但是，如果已刪除設定檔資訊或系統中安裝了另一個顯示驅動程式，DrawDib 會重新運行測試。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DrawDib 函式](about-the-drawdib-functions.md)
</dt> </dl>

 

 




