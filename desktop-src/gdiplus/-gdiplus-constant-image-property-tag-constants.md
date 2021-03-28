---
description: 有數種影像檔案格式可讓您儲存中繼資料和影像。
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: 影像屬性標記常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972916"
---
# <a name="image-property-tag-constants"></a>影像屬性標記常數

有數種影像檔案格式可讓您儲存中繼資料和影像。 中繼資料是關於影像的資訊，例如標題、寬度、相機型號和演出者。 Windows GDI + 提供統一的方式，可讓您以標記的影像檔案格式儲存和取出影像檔案的中繼資料， (TIFF) 、JPEG、便攜網狀圖形 (PNG) 和交換影像檔案 (EXIF) 格式。

在 GDI + 中，中繼資料的部分稱為 *屬性專案*，而個別屬性專案則是由稱為 *屬性標記* 的數值常數來識別。 您可以藉由呼叫 [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 [**Image：： SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem)和 [**image：： GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem)方法來儲存和取出中繼資料，而不需要擔心特定檔案格式儲存該中繼資料的詳細資料。

下列主題將列出並描述 GDI + 所支援的屬性專案。 描述很簡單且一般，因此適用于各種不同的檔案格式。 如需有關如何在特定檔案格式中使用屬性專案的詳細說明，請參閱該檔案格式的規格。 如需多個檔案格式規格的連結，請參閱 [影像檔案格式規格](-gdiplus-constant-image-file-format-specifications.md)。 如需中繼資料的詳細資訊，請參閱 [讀取和寫入中繼資料](-gdiplus-reading-and-writing-metadata-use.md) 和 [**影像屬性標記類型常數**](-gdiplus-constant-image-property-tag-type-constants.md)。

-   [以數位順序排序的屬性標記](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [依字母順序排列的屬性標記](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [屬性專案描述](-gdiplus-constant-property-item-descriptions.md)

 

 



