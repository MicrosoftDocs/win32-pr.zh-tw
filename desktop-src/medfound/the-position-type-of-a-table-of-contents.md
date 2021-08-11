---
description: 目錄的位置類型
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: 目錄的位置類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f94f23e185b46f52123a80a0d27f7fefffcaff7e711a5e9718e07dab7da40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237892"
---
# <a name="the-position-type-of-a-table-of-contents"></a>目錄的位置類型

[**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser)介面的某些方法有一個名為 *enumTocPosType* 的參數，其類型為 [**enum TOC \_ POS \_ 型**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type)別。 此參數會指定媒體檔案中儲存目錄的位置。 其目的是要將目錄儲存在檔案標頭中，或儲存在檔案的主體中，做為最上層物件。 這種功能尚未實行。

目前，目錄只能儲存為最上層的物件，因此您必須一律將 *enumTocPosType* 參數設定為 **TOC \_ POS \_ TOPLEVELOBJECT**。 如果您將 *enumTocPosType* 設定為 **TOC \_ POS \_ INHEADER**，此方法將會傳回 **E \_ >notimpl**。

下列方法具有 *enumTocPosType* 參數。

-   [**GetTocCount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**GetTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**RemoveTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**RemoveTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[目錄剖析器程式設計指南](toc-parser-programming-guide.md)
</dt> </dl>

 

 



