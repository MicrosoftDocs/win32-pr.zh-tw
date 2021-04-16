---
title: MIDL 編譯
description: MIDL 編譯
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463757"
---
# <a name="midl-compilation"></a>MIDL 編譯

給定 IDL 檔案（如 [Example2](anatomy-of-an-idl-file.md)），它會定義一或多個 COM 介面和類型程式庫，MIDL 編譯器 (Midl.exe) 會產生下表中所述的檔案做為預設輸出。



| 檔案名稱                 | 描述                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Example2。h<br/>    | 標頭檔案，其中包含 IDL 檔案中定義之所有介面的類型定義和函式宣告，以及存根所呼叫之常式的向前宣告。<br/> |
| Example2 \_ p. c<br/> | Proxy/stub 檔案，其中包含用戶端和伺服器的代理進入點。<br/>                                                                                           |
| Example2 \_ c。<br/> | 介面識別碼檔案，這個檔案會定義 IDL 檔案中指定之每個介面的 GUID。<br/>                                                                                               |
| Example2 .tlb<br/>  | 複合檔案檔案，其中包含類型和物件的相關資訊。<br/>                                                                                                                |
| Dlldata.c。c<br/>     | 包含建立 proxy/stub DLL 所需的資料。<br/>                                                                                                                                     |



 

當用戶端應用程式和物件服務器使用此檔案時，您可以使用標頭檔和所有 .c 檔案來建立可支援介面的 [PROXY DLL](building-and-registering-a-proxy-dll.md) 。 \_當您為使用介面的用戶端應用程式建立可執行檔時，您可以使用 (Example2 的介面標頭檔) 和介面識別碼 (Example2 的) 檔。 您可以選擇在 EXE 或 DLL 中以資源的形式包含類型程式庫檔案，也可以將它當作個別檔案來傳送。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[針對 COM 介面產生的檔案](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[MIDL 編譯器選項](midl-compiler-options.md)
</dt> </dl>

 

