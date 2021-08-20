---
title: 針對 COM 介面產生的檔案
description: 針對 COM 介面，MIDL 編譯器會將所有用戶端和物件服務器輔助常式和資料結合成單一介面 proxy 檔案。
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL 編譯器 MIDL、MIDL 和 COM
- COM MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efed184c8fe241a0028b210a33f695bec197a4a6591e8837e0e2e0343ee4ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991336"
---
# <a name="files-generated-for-a-com-interface"></a>針對 COM 介面產生的檔案

針對 COM 介面，MIDL 編譯器會將所有用戶端和物件服務器輔助常式和資料結合成單一介面 proxy 檔案。 此檔案包含用戶端和伺服器的代理進入點。 此外，MIDL 編譯器會產生介面標頭檔、介面 UUID 檔案和介面註冊檔案。 在建立包含程式碼的 proxy DLL 時，您將會使用這些檔案，以支援用戶端應用程式和物件服務器的介面使用。 當您為使用介面的用戶端應用程式建立可執行檔時，您也會使用介面標頭檔和介面 UUID 檔。

下列主題描述針對自訂 COM 介面產生的每個檔案，您可以 **\[** [](object.md) **\]** 在 IDL 檔案的介面屬性清單中包含物件屬性來識別這些檔案：

-   [介面 Proxy 檔案](the-interface-proxy-file.md)
-   [標頭檔](the-header-files.md)
-   [介面 UUID 檔案](the-interface-uuid-file.md)
-   [介面註冊檔案](the-interface-registration-file.md)

如需詳細資訊，請參閱 [應用程式佈建檔 (ACF)](application-configuration-file-acf-.md)、 [**/App \_ config**](-app-config.md)、 [介面定義 (IDL)](interface-definition-idl-file.md)檔案，以及 [建立和註冊 Proxy DLL](../com/building-and-registering-a-proxy-dll.md)。

 

 