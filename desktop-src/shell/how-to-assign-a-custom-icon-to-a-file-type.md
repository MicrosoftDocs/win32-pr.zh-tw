---
description: 您必須將自訂圖示指派給檔案類型，以提供視覺指示給該檔案類型的使用者，或與檔案類型相關聯的應用程式。
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: 如何將自訂圖示指派給檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973181"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>如何將自訂圖示指派給檔案類型

當沒有任何自訂預設圖示指派給檔案類型時，桌面和 Windows 檔案總管會以一般預設圖示來顯示該類型的所有檔案。 例如，下列螢幕擷取畫面顯示與 MyDocs4. myp 檔案搭配使用的預設圖示。

![預設圖示的螢幕擷取畫面](images/icon.png)

雖然在此螢幕擷取畫面中顯示的所有檔案都是簡單的文字檔，但只有 MyDocs4 會顯示 Windows 預設圖示。 這是因為 .txt 副檔名是具有自訂預設圖示的已註冊檔案類型。

下列螢幕擷取畫面顯示已指派給 myp 檔案類型的自訂圖示。

![myp 檔案自訂圖示的螢幕擷取畫面](images/context4.png)

> [!Note]  
> 您也可以在應用程式特定的基礎上指派圖示。

 

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

在下列兩個位置的其中一個位置建立名為 **DefaultIcon** 的子機碼：

-   針對檔案類型指派， **HKEY 類別的 \_ \_ 根目錄** \\ *副檔名*
-   針對應用程式指派， **HKEY \_ 類別 \_ 根目錄** \\ *ProgID*

### <a name="step-2"></a>步驟 2:

指派 **DefaultIcon** 子機碼為 **REG \_ SZ** 類型的預設值，指定包含圖示之檔案的完整路徑。

### <a name="step-3"></a>步驟 3：

呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 函數，以通知 Shell 更新其圖示快取。

## <a name="remarks"></a>備註

下列範例會詳細說明檔案類型圖示指派所需的登錄專案。 副檔名是與應用程式相關聯，但圖示指派是在副檔名本身，因此相關聯的應用程式不會指定預設圖示。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

下列範例顯示應用程式圖示指派所需的登錄專案詳細觀點。 Myp 副檔名會先與 Myprogram.exe. 1 應用程式相關聯。 接著會將自訂預設圖示指派給 Myprogram.exe. 1 ProgID 子機碼。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

任何包含圖示的檔案都是可接受的，包括 .ico、.exe 和 .dll 檔案。 如果檔案中有一個以上的圖示，路徑後面應該接著逗號，再接著圖示的索引。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案類型](fa-file-types.md)
</dt> </dl>

 

 



