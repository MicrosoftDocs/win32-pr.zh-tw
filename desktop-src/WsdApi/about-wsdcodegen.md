---
description: 描述 WsdCodeGen 所使用的輸入檔，以及 WsdCodeGen 所產生的輸出檔。
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: 關於 WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026542"
---
# <a name="about-wsdcodegen"></a>關於 WsdCodeGen

WsdCodeGen 會使用 XML 設定檔來判斷服務中繼資料的位置。 設定檔也用來定義介面名稱、介面 Guid、類別名稱、方法名稱和其他識別碼。 如需此檔案的詳細資訊，請參閱 [WsdCodeGen 設定檔](wsdcodegen-configuration-file.md)。

WsdCodeGen 需要兩種類型的輸入檔： XML 設定檔，以及一或多個服務描述檔案 (WSDL 和/或 XSD 檔案) 。 WsdCodeGen 會處理這些輸入檔案，並產生兩種類型的輸出檔案：介面檔案和標頭/來源檔案。

## <a name="input-files"></a>輸入檔



| 類型                      | Description                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 組態檔        | XML 檔案，表示服務中繼資料的位置，並定義介面名稱、介面 Guid、類別名稱、方法名稱和其他識別碼。 |
| 服務描述檔案 | 描述要在裝置上執行之服務的一或多個 WSDL 或 XSD 檔案。                                                                           |



 

## <a name="output-files"></a>輸出檔



| 類型                        | Description                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 介面檔             | IDL (介面定義語言) 檔案，可搭配 MIDL 編譯器使用以產生介面標頭檔。 WSDAPI 用戶端和 WSDAPI 服務可以使用此介面檔。                                                                                                                                                           |
| C + + 標頭檔和原始檔 | 描述訊息合約、命名空間和類型資訊的 c + + 檔案。 它們可能包含 proxy 程式碼和/或 stub 程式碼。 Proxy 程式碼會執行服務的介面，並將服務方法呼叫轉譯為發出服務要求的 WSDAPI 作業。 Stub 程式碼會將 WSDAPI 服務要求轉譯為呼叫服務方法的程式碼。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置上的 Web 服務程式碼產生器](web-services-for-devices-code-generator.md)
</dt> <dt>

[使用 WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 



