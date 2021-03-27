---
description: 您可以使用 CreateEnhMetaFile 函式來建立增強的中繼檔，以提供適當的引數。
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: 增強的中繼檔建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080c350e41e895c5d4bf834a6f407cca5907743d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691884"
---
# <a name="enhanced-metafile-creation"></a>增強的中繼檔建立

您可以使用 [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) 函式來建立增強的中繼檔，以提供適當的引數。 系統會使用這些引數來維護圖片尺寸、判斷中繼檔是否應該儲存在磁片或記憶體中等等。

若要跨輸出裝置維護圖片尺寸， [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) 需要解析參考裝置。 此 *參照裝置* 是圖片第一次出現的裝置，而 *參考 DC* 則是與參考裝置相關聯的 *裝置內容* 。 呼叫 **CreateEnhMetaFile** 函式時，您必須提供識別此 DC 的控制碼。 您可以藉由呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 或 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函數來取得此控制碼。 您也可以指定 **Null** 做為控制碼，以使用目前的顯示裝置作為參考裝置。

大部分的應用程式會永久儲存圖片，因而建立儲存在磁片上的增強中繼檔;不過，在某些情況下並不需要這麼做。 例如，提供圖表繪圖功能的文書處理應用程式，可以將使用者定義的圖表以增強中繼檔的形式儲存在記憶體中，然後將增強的中繼檔位從記憶體複製到使用者的檔檔案中。 需要在磁片上永久儲存之中繼檔的應用程式，必須在呼叫 [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)時提供檔案名。 如果未提供檔案名，系統會自動將中繼檔視為暫存檔案，並將它儲存在記憶體中。

您可以在包含圖片和作者相關資訊的中繼檔中加入選擇性的文字描述。 應用程式可以在 [開啟檔案] 對話方塊中顯示這些字串，為使用者提供可協助您選取適當檔案的中繼檔內容相關資訊。 如果應用程式包含文字描述，則在呼叫 [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)時，必須提供指向字串的指標。

當 [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) 成功時，它會傳回一個控制碼來識別特殊的中繼檔裝置內容。 中繼檔裝置內容是唯一的，因為它會與檔案相關聯，而不是輸出裝置。 當系統處理接收到中繼檔裝置內容之控制碼的 GDI 函式時，它會將 GDI 函數轉換成增強的中繼檔記錄，並將記錄附加至增強型中繼檔的結尾。

在圖片完成並將最後一筆記錄附加至增強型中繼檔之後，應用程式可以藉由呼叫 [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) 函式來關閉檔案。 此函式會關閉並刪除特殊的中繼檔裝置內容，並傳回識別增強中繼檔的控制碼。

若要刪除增強格式的中繼檔或增強格式的中繼檔控制碼，請呼叫 [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile) 函數。

 

 



