---
title: MIDL 編譯器
description: MIDL 編譯器
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db4afbbe8c7a82f4335855b40e578fe2eea046fa4c7f0560e3e297b559a67ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736427"
---
# <a name="midl-compiler"></a>MIDL 編譯器

MIDL 編譯器會處理 IDL 檔案，以產生類型程式庫和輸出檔案。 MIDL 編譯器所產生之輸出檔的類型取決於 IDL 檔案的介面屬性清單中指定的屬性。

如果屬性清單包含 \[ [**object**](/windows/desktop/Midl/object) \] 關鍵字，MIDL 編譯器會產生 COM 介面輸出檔案：介面 proxy 檔案、介面標頭檔，以及介面 (GUID) 檔的全域唯一識別碼。 如果 IDL 檔案包含連結 [**庫**](/windows/desktop/Midl/library) 語句，MIDL 會產生具有 .tlb 副檔名的類型程式庫檔案。 如果 IDL 檔案中有任何介面沒有 \[ **object** \] 關鍵字，且未包含在連結 **庫** 語句中，MIDL 編譯器會針對遠端程序呼叫產生適當的介面輸出檔， (rpc) ：用戶端 stub 檔案、伺服器 stub 檔案和標頭檔。 如需詳細資訊，請參閱主題 [介面定義和類型程式庫](/windows/desktop/Midl/interface-definitions-and-type-libraries) ，以及 [使用 MIDL 產生類型程式庫](/windows/desktop/Midl/generating-a-type-library-with-midl-2)。

從 IDL 檔案產生類型程式庫和輸出檔案：

-   從命令提示字元中，執行

    **midl** *檔案名*

    其中 *filename* 是 IDL 檔案的名稱。

MIDL 編譯器也支援數個選擇性參數。 如需完整清單，請參閱 Visual C++ 檔中的「MIDL Command-Line 參考」，或執行下列命令列：

**midl/？**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft 介面定義語言](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[轉換成 c + +](translating-to-c--.md)
</dt> </dl>

 

 