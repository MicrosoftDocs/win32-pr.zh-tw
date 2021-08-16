---
title: '應用程式佈建檔 (ACF) '
description: 您的分散式應用程式可能會影響某個元件，但與另一個元件無關。
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- ACF MIDL
- Microsoft 介面定義語言 MIDL，描述，應用程式佈建檔案
- 應用程式佈建檔 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56158267a11125a825442b4db98224d292fdfc309f79cb1562818dee9c08aa23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808340"
---
# <a name="application-configuration-file-acf"></a>應用程式佈建檔 (ACF) 

您的分散式應用程式可能會影響某個元件，但與另一個元件無關。 例如，物件可能包含大型的複雜資料結構，並將此資料結構的內容傳遞至另一個物件。 對接收應用程式而言，此資料結構的確切版面配置可能沒有意義。 此外，此結構可能包含 MIDL 編譯器無法辨識的資料類型，而且無法產生封送處理和封送處理常式代碼。

用戶端應用程式可以共用相同的介面，但在不同的平臺上執行;它們可能每一個都需要自己的封送處理常式集。 最後，個別用戶端不一定需要相同的函式集合。 針對將永遠不會在特定用戶端應用程式中執行的函式產生 stub 程式碼，會產生效率不佳的情況。

藉由在應用程式佈建檔中定義介面的這些本機層面 (ACF) ，您可以將用戶端介面的差異與其網路表示分開，讓伺服器以一致的格式來傳送和接收資料，並讓您的存根程式碼更簡潔且更有效率。

ACF 介面定義的結構和語法與 IDL 定義相同：

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

根據預設，ACF 介面名稱必須與 IDL 定義中的名稱相符。 但是，當您使用 MIDL 編譯器選項/ [**acf**](-acf.md) 明確指定 acf 檔案名時，介面名稱不一定要相符。 這項功能可讓數個介面共用單一 ACF 規格。

 

 




