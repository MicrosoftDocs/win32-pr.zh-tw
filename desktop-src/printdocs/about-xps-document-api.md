---
description: xps 檔 API 會執行 xps 物件模型，並可讓開發人員建立 xps om、操作原生 Windows 程式中的 xps 檔內容 \\ \\ ，並將 xps om 儲存為檔案或串流作為 xps 檔。
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: 關於 XPS 檔 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b2363bba55fed184b1cf80bfc81fac9474444f77c9b867b461940e6b72d8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950908"
---
# <a name="about-xps-document-api"></a>關於 XPS 檔 API

[xps 檔 API](documents-xps.md)會執行 xps 物件模型，並可讓開發人員建立 xps om、操作原生 Windows 程式中的 xps 檔內容 \\ \\ ，並將 xps om 儲存為檔案或串流作為 xps 檔。 XPSDrv 篩選管線模組的開發人員也可以使用 XPS 檔 API，在 XPSDrv 印表機驅動程式篩選器中操作 XPS 檔內容。

## <a name="xps-document-api-overview"></a>XPS 檔 API 總覽

XPS 物件模型是 XPS 檔的資訊模型。 XPS 檔的資訊模型與檔元件內使用的標記模型不同。 XPS 物件模型會描述組成 XPS 檔的內部元件組織，而標記模型則會描述這些元件的內容。

在程式中，XPS 物件模型會以 XPS OM 的形式具現化。 XPS OM 本質上是 XPS 檔內容的記憶體中版本。 在將邏輯組織與 XPS 檔類似的情況下，XPS OM 在序列化為檔案或資料流程之前，都不會被視為 XPS 檔。

當 XPS 檔從標記還原序列化為 XPS OM 時，XPS OM 無法使用正確的標記結構。 例如，無論屬性是以專案或標記中的屬性工作表示，XPS OM 都會以完全相同的方式來呈現檔物件的屬性值。

[XPS 檔 API](documents-xps.md)可分為下列類別：

-   [XPS OM 主幹介面](xps-om-trunk-interfaces.md)

    主幹介面可讓您存取 XPS 檔結構的最上層元件。 這些介面也提供序列化 XPS OM 和還原序列化 XPS 檔的方法。

-   [XPS OM 頁面介面](xps-object-model-page-interfaces.md)

    頁面介面可讓您存取 XPS 檔中的頁面內容。 描述頁面內容的介面也會包含在頁面介面中。

-   [XPS OM 數位簽章](using-the-xps-digital-signatures.md)

    XPS OM 支援數位簽章。 不過，您可以直接存取 XPS 檔中的數位簽章，而不需要建立 XPS OM。 如需有關如何在不使用 XPS OM 的情況下存取 XPS 數位簽章的詳細資訊，請參閱 [Xps 數位簽章 API](xps-digital-signatures.md)。

-   [XPS OM 列印票證介面](xps-object-model-print-ticket-interfaces.md)

    XPS 檔支援封裝的列印票證 (作業) 、檔和頁面層級。 列印票證包含有關如何格式化檔內容以進行列印或觀看的資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**本節內容**
</dt> <dt>

[XPS OM 主幹介面](xps-om-trunk-interfaces.md)
</dt> <dt>

[XPS OM 頁面介面](xps-object-model-page-interfaces.md)
</dt> <dt>

[XPS OM 數位簽章](using-the-xps-digital-signatures.md)
</dt> <dt>

[XPS OM 列印票證介面](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

**其他相關主題**
</dt> <dt>

[初始化 XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[XPS OM 數位簽章](using-the-xps-digital-signatures.md)
</dt> <dt>

[XPS 檔 API 參考](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



