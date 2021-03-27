---
description: 曲線路徑
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: 曲線路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848569"
---
# <a name="curved-paths"></a>曲線路徑

應用程式可以藉由呼叫 [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) 函式來壓平合併路徑中的曲線。 此函式特別適用于將文字放在包含曲線的路徑輪廓上的應用程式。 為了符合文字，應用程式必須執行下列步驟：

1.  建立文字出現的路徑。
2.  呼叫 [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) 函數，將路徑中的曲線轉換成線段。
3.  呼叫 [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) 函式來取出這些線段。
4.  計算每一行的長度，以及字串中每個字元的寬度。
5.  使用線條寬度和字元寬度資料，沿著曲線放置每個字元。

 

 



