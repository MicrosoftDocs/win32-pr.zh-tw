---
title: 介面 UUID 檔案
description: 介面 UUID 檔會從已處理的 IDL 檔案中的所有介面收集介面識別碼的定義。
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL 和 COM MIDL、介面、proxy UUID 檔案
- 介面 UUID 檔案 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d12986ee265fa50f440dd07812d222bb4e7549a6c32c93938803255480871f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146201"
---
# <a name="the-interface-uuid-file"></a>介面 UUID 檔案

介面 UUID 檔會從已處理的 IDL 檔案中的所有介面收集介面識別碼的定義。 類似于存根檔和標頭檔，輸入資料流程關閉是由目前的 IDL 檔案和包含的檔案所定義。 例如，針對介面 IFace，編譯器會產生常數 IID \_ IFace，並將它初始化為 IDL 檔案中指定的介面 UUID。 用戶端應用程式和 proxy DLL 會使用這個常數來識別介面。

從檔案產生之介面 IID 檔案的預設名稱。 .idl 為 File \_ i.c。 [**/Iid**](-iid.md) MIDL 編譯器參數會覆寫介面 UUID 檔案的預設名稱。

 

 




