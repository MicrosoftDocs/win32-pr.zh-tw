---
description: 您可以使用增強型中繼檔的控制碼來完成下列工作：
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: 增強的中繼檔作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5daf08ef5d8d48b81aea4daa5d2696ececec3fce44b1303c9ff7ccd692151a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250282"
---
# <a name="enhanced-metafile-operations"></a>增強的中繼檔作業

您可以使用增強型中繼檔的控制碼來完成下列工作：

-   顯示儲存在增強型中繼檔中的圖片。
-   建立增強型中繼檔的複本。
-   編輯增強的中繼檔。
-   取出儲存在增強型中繼檔中的選擇性描述。
-   取出增強型中繼檔標頭的複本。
-   取出增強型中繼檔的二進位版本。
-   列舉選擇性調色板中的色彩。

本主題其餘部分的各節將討論這些工作。

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>顯示儲存在增強型中繼檔中的圖片

您可以使用 [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) 函式來顯示儲存在增強型中繼檔中的圖片。 將函式傳遞給增強中繼檔的控制碼，而不需要考慮增強型中繼檔記錄的格式。 不過，有時候您會想要列舉增強中繼檔中的記錄，以搜尋特定的 GDI 函數，並以某種方式修改函式的參數。 若要這樣做，您可以使用 [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) 並提供回呼函數 [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)，以處理增強的中繼檔記錄。 若要修改增強型中繼檔記錄的參數，您必須知道記錄中的參數格式。

## <a name="create-copies-of-an-enhanced-metafile"></a>建立增強型中繼檔的複本

有些應用程式會在讓使用者改變原始檔之前，建立暫存備份 (或複製檔案的) 複本。 應用程式可以藉由呼叫 [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) 函式、提供識別增強型中繼檔的控制碼，以及提供新檔案名稱的指標，建立增強型中繼檔的備份複本。

若要建立以記憶體為基礎的增強格式中繼檔，請呼叫 [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits) 函數。

## <a name="edit-an-enhanced-metafile"></a>編輯增強的中繼檔

大部分繪圖、圖例以及電腦輔助設計 (CAD) 應用程式都需要一種方式來編輯儲存在增強中繼檔中的圖片。 雖然編輯增強的中繼檔是很複雜的工作，但是您可以搭配其他函式使用 [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) 函式，以在您的應用程式中提供這項功能。 **EnumEnhMetaFile** 函式和其相關聯的回呼函數 [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)，可讓應用程式處理增強中繼檔中的個別記錄。

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>取出儲存在增強型中繼檔中的選擇性描述

有些應用程式會在 [ **開啟** ] 對話方塊中，以對應的檔案名顯示增強型中繼檔的文字描述。 您可以使用 [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) 函式來抓取中繼檔標頭，並檢查其中一個成員，以判斷這個字串是否存在於增強的中繼檔中。 如果字串存在，應用程式會藉由呼叫 [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona) 函式來進行抓取。

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>取出增強型中繼檔的二進位版本

您可以藉由呼叫 [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) 函數來取出中繼檔的內容;不過，在抓取內容之前，您必須指定檔案的大小。 若要取得大小，您可以使用 [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) 函數，並檢查適當的成員。

## <a name="enumerate-the-colors-in-the-optional-palette"></a>列舉選擇性調色板中的色彩

若要在各種輸出裝置上顯示圖片時達到一致的色彩，您可以呼叫 [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) 函式，並將邏輯調色板儲存在增強的中繼檔中。 顯示儲存在增強型中繼檔中之圖片的應用程式會抓取這個調色板，並在顯示圖片之前呼叫 [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) 函式。 若要判斷調色板是否儲存在增強型中繼檔中，請取出中繼檔標頭，並檢查適當的成員。 如果有調色板，您可以呼叫 [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) 函式來取出邏輯調色板。

 

 
