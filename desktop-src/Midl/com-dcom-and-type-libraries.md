---
title: COM、DCOM 和型別程式庫
description: 元件物件模型 (COM) 和分散式元件物件模型 (DCOM) 使用遠端程序呼叫 (RPC) ，讓分散式元件物件能夠彼此通訊。
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- 介面 MIDL、COM
- 介面 MIDL、DCOM
- 介面 MIDL、類型程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997d2a61fef3e2bc46f4539dca2ecd67d8de385d402e5e9c862b267b697b3cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991758"
---
# <a name="com-dcom-and-type-libraries"></a>COM、DCOM 和型別程式庫

元件物件模型 (COM) 和分散式元件物件模型 (DCOM) 使用遠端程序呼叫 (RPC) ，讓分散式元件物件能夠彼此通訊。 因此，COM 或 DCOM 介面會定義 COM 物件的身分識別和外部特性。 它會形成用戶端存取物件方法和資料的方式。 使用 DCOM，不論物件是否存在於相同的進程中、相同電腦上的不同進程，或不同的電腦上，都可以存取此存取。 如同 RPC 用戶端/伺服器介面，COM 或 DCOM 物件可以透過數種不同的方式和多個介面來公開其功能。

## <a name="type-library"></a>類型程式庫

類型程式庫 ( .tlb) 是一種二進位檔案，它會將 COM 或 DCOM 物件的屬性和方法的相關資訊儲存在執行時間可供其他應用程式存取的表單中。 使用類型程式庫，應用程式或瀏覽器可以判斷物件支援的介面，以及叫用物件的介面方法。 即使物件和用戶端應用程式是以不同的程式設計語言撰寫，也可能會發生這種情況。 COM/DCOM 執行時間環境也可以使用類型程式庫，為類型程式庫中所述的介面提供自動跨單元、跨進程和跨電腦封送處理。

## <a name="characteristics-of-an-interface"></a>介面的特性

您可以在介面定義中定義介面的特性， (IDL) 檔和選擇性的應用程式佈建檔 (ACF) ：

-   IDL 檔案指定應用程式介面在網路上的特性，也就是在用戶端與伺服器之間，或在 COM 物件之間傳輸資料的方式。
-   ACF 檔案會指定僅與本機作業環境相關的介面特性，例如系結控制碼。 ACF 檔案也可以指定如何在獨立于電腦的表單中封送處理和傳輸複雜的資料結構。

如需 IDL 和 ACF 檔案的詳細資訊，請參閱 [idl 和 ACF](/windows/desktop/Rpc/the-idl-and-acf-files)檔案。

IDL 和 ACF 檔案是以 Microsoft 介面定義語言撰寫的腳本 (MIDL) ，也就是憑證-DCE 介面定義語言 (IDL) 的 Microsoft 執行和延伸模組。 IDL 語言的 Microsoft 擴充功能可讓您建立 COM 介面和類型程式庫。 編譯器 Midl.exe 會使用這些腳本來產生 C 語言的存根和標頭檔，以及類型程式庫檔案。

## <a name="the-midl-compiler"></a>MIDL 編譯器

根據 IDL 檔案的內容而定，MIDL 編譯器將會產生下列任何檔案。

C 語言 proxy/stub 檔案、介面識別碼檔案、DLL 資料檔案，以及自訂 COM 介面的相關標頭檔。 當 MIDL 編譯器遇到介面屬性清單中的物件屬性時，會產生這些檔案。 如需這些檔案的詳細資訊，請參閱 [針對 COM 介面產生的](files-generated-for-a-com-interface.md)檔案。

已編譯的類型程式庫 ( .tlb) 檔案和相關標頭檔。 當 MIDL 遇到 IDL 檔案中的連結 [**庫**](library.md) 語句時，會產生這些檔案。 如需型別程式庫的一般資訊，請參閱《 Automation 程式設計人員參考》中的 [類型程式庫內容](/previous-versions/windows/desktop/automat/contents-of-a-type-library)。

C/c + +-語言用戶端和伺服器 stub 檔案，以及 RPC 介面的相關標頭檔。 當 IDL 檔案中沒有 [**物件**](object.md) 屬性的介面時，就會產生這些檔案。 如需存根和標頭檔的總覽，請參閱 [一般組建](/windows/desktop/Rpc/general-build-procedure)程式。 如需詳細資訊，請參閱 [針對 RPC 介面產生的](files-generated-for-an-rpc-interface.md)檔案。

 

 