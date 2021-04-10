---
description: 建立基礎語言資源檔
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: 建立基礎語言資源檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027362"
---
# <a name="creating-the-base-language-resource-file"></a>建立基礎語言資源檔

使用者介面專案的資源是針對應用程式所支援的基礎語言而定義，例如，英文 (美國) 。 Win32 PE 資源檔的範例是使用 RC 編譯器建立的 .rc 檔。 如需建立 .rc 檔的詳細資訊，請參閱 [關於資源檔](../menurc/about-resource-files.md)。

如果使用基礎語言資源的 .rc 檔，您可以選擇使用資源設定檔來表示資源設定資料的 XML 表示。 若要建立這個檔案，請參閱 [準備資源設定檔](preparing-a-resource-configuration-file.md)。

您也可以使用非 Win32 PE 檔案來定義基礎語言資源。 例如，您可以針對此用途使用 .xml 檔案或 .txt 檔案。

> [!Note]  
> 當您使用非 Win32 PE 檔案來定義基礎語言資源時，不能使用 RC 編譯器進行資源定義。 相反地，您會定義自己的資源格式，而您的應用程式必須提供自己的功能，以尋找並載入所需的資源。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[準備資源](preparing-resources.md)
</dt> <dt>

[準備資源設定檔](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
