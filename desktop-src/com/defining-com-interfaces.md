---
title: 定義 COM 介面
description: Microsoft 會定義許多 COM 介面。 在大多數情況下，您可以重複使用這些泛型介面。 不過，有些應用程式有特定需求，因此需要或需要定義您自己的物件介面。
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e676172e51fca810f0cbb7ba93b5d52b814319b6e8b890f20ba9c51617f7ac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071018"
---
# <a name="defining-com-interfaces"></a>定義 COM 介面

Microsoft 會定義許多 COM 介面。 在大多數情況下，您可以重複使用這些泛型介面。 不過，有些應用程式有特定需求，因此需要或需要定義您自己的物件介面。

所有 COM 介面都必須直接或間接衍生自 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面。 在該條件約束內，您的自訂介面幾乎可以支援任何方法或參數，包括非同步方法。 您也可以為自訂介面產生類型程式庫，讓用戶端可以在執行時間存取物件方法的相關資訊。 在您定義介面之後，請使用 Microsoft 介面定義語言 (MIDL) 來加以描述、編譯並註冊它，就像使用任何泛型介面一樣。 使用分散式 COM 時，介面方法可用於遠端進程以及相同電腦上的其他進程。

最後，建立 COM 介面需要一個包含 C/c + + 編譯器和 Midl.exe 編譯器的開發環境。

建立 COM 介面的步驟如下：

-   決定您要如何為您的介面提供封送處理支援;使用類型程式庫驅動封送處理，或使用 proxy/stub DLL。 即使同進程介面要跨多個範圍界限使用，也必須封送處理。 最好是將封送處理支援建立至每個 COM 介面，即使您不認為您將需要它。 如需詳細資訊，請參閱 [介面封送處理](interface-marshaling.md) 。
-   描述介面定義中的介面或介面 (IDL) 檔。 此外，您可以在應用程式佈建檔中指定介面的特定本機層面 (ACF) 。 如果您使用類型程式庫驅動封送處理，請新增連結 [**庫**](/windows/desktop/Midl/library) 語句，以參考您要產生類型資訊的介面。
-   使用 MIDL 編譯器來產生類型程式庫檔案和標頭檔案，或 C 語言 proxy/stub 檔案、介面識別碼檔案、DLL 資料檔案和標頭檔。 如需詳細資訊，請參閱 [MIDL 編譯](midl-compilation.md) 。
-   根據您選擇的封送處理方法，將模組定義寫入 (DEF) 檔案、將所有 MIDL 產生的檔案編譯並連結到單一 proxy DLL 中，並在系統登錄中註冊介面，或註冊類型程式庫。 如需詳細資訊，請參閱 [載入和註冊類型程式庫](loading-and-registering-a-type-library.md) ，以及 [建立和註冊 Proxy DLL](building-and-registering-a-proxy-dll.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IDL 檔案的剖析](anatomy-of-an-idl-file.md)
</dt> <dt>

[COM 用戶端和伺服器](com-clients-and-servers.md)
</dt> <dt>

[介面設計規則](interface-design-rules.md)
</dt> <dt>

[元件物件模型](the-component-object-model.md)
</dt> </dl>

 

 