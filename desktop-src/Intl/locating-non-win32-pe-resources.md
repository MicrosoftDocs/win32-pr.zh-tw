---
description: 尋找非 Win32 PE 資源
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: 尋找非 Win32 PE 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf706712b2e1be2dd8fb1598c1404a829251bb24db83db7c7d6deaa87a13d24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147171"
---
# <a name="locating-non-win32-pe-resources"></a>尋找非 Win32 PE 資源

若要尋找非 Win32 PE 資源，您的應用程式應該先呼叫 [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) 函式，以找出要從中載入資源的特定語言資源檔。 如果應用程式是遵循系統語言設定，則必須使用針對 DwFlags 指定的 \_ mui \_ 語言 \| 名稱 mui \_ 使用者慣用 UI 語言來呼叫函式，並為 \_ \_ \_ *pwszLanguage* 指定 **Null** 。  如果應用程式是依照應用程式特定的語言設定，則會使用 **GetFileMUIPath** ，藉由在 *pwszLanguage* 參數中指定語言來判斷特定語言的檔案是否存在。

呼叫 [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)之後，應用程式必須定義自訂功能以載入資源模組，並從中載入特定資源。 例如，如果您使用 .txt 或 .xml 資源檔，應用程式必須使用 TXT 或 XML 剖析器來載入檔案，然後針對每個必要的資源剖析檔案的內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用多語系消費者介面](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



