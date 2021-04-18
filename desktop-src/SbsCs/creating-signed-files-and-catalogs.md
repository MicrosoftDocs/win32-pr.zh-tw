---
description: 若要簽署檔案並為其建立目錄，您必須先擁有簽署檔案、憑證和公開金鑰的程式。
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: 建立已簽署的檔案和目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193088"
---
# <a name="creating-signed-files-and-catalogs"></a>建立已簽署的檔案和目錄

若要簽署檔案並為其建立目錄，您必須先擁有簽署檔案、憑證和公開金鑰的程式。

**簽署檔案和建立目錄**

1.  使用 [Pktextract.exe](pktextract-exe.md) 從憑證檔案中解壓縮 [*公開金鑰 token*](p-sbscs-gly.md) 。 憑證檔案必須存在於與公用程式相同的目錄中。
2.  使用公開金鑰 token 值，在資訊清單檔中更新 **assemblyIdentity** 元素的 **publicKeyToken** 屬性。
3.  使用 [MT.exe](mt-exe.md) 來產生組件資訊清單中包含的檔案雜湊，以及建立目錄描述檔案 ( 的 cdf) 。
4.  使用 Makecat.exe 搭配產生的 cdf 來建立元件的安全性目錄。 此工具組含在 CryptoAPI 中。
5.  使用 [SignTool](/windows/desktop/SecCrypto/signtool) 公用程式來簽署使用步驟1中所使用之憑證所產生的目錄。 建立目錄之後，就可以刪除步驟3和4中的 cdf。

另請參閱 [元件簽署範例](assembly-signing-example.md)。

 

 
