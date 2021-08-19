---
title: 介面註冊檔案
description: 介面註冊檔案會收集可協助您註冊封裝至 DLL 或 EXE 檔案之 COM 介面的資訊。
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- 介面註冊檔 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a5541a5e60b1903364236f86dcf1845a5e1ac153fc91b47bacf9f553a9a109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806176"
---
# <a name="the-interface-registration-file"></a>介面註冊檔案

介面註冊檔案會收集可協助您註冊封裝至 DLL 或 EXE 檔案之 COM 介面的資訊。 介面註冊檔案與其他產生的檔案不同，因為它可以從編譯數個不同的 IDL 檔案收集資訊。 COM 介面執行的每個 MIDL 編譯器會先尋找現有的 dlldata.c .c 檔案，如果找不到該檔案，就會建立新的 dlldata.c .c 檔案。 如果找到 dlldata.c 檔案，則會將目前 IDL 的相關資訊新增 (如果) 或已取代。

介面註冊檔會在多處理器環境中安全地產生或更新，因為平行 MIDL 編譯無法同時寫入檔案。 因為任何 dlldata.c 檔都可以由組建環境或使用者標記為唯讀，所以 MIDL 編譯器會執行超時方法來等候無法開啟的檔案，並在超時時間過期時發出適當的錯誤訊息。

從輸入檔產生之介面註冊檔的預設名稱是 dlldata.c。 [**/Dlldata**](-dlldata.md) MIDL 編譯器參數可以用來覆寫檔案的預設名稱。 當封裝至通用二進位檔的某些 IDL 檔案位於不同的目錄時，覆寫介面註冊檔案的預設名稱特別有用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立和註冊 Proxy DLL](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 