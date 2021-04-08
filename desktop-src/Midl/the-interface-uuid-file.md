---
title: 介面 UUID 檔案
description: 介面 UUID 檔會從已處理的 IDL 檔案中的所有介面收集介面識別碼的定義。
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL 和 COM MIDL、介面、proxy UUID 檔案
- 介面 UUID 檔案 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675171"
---
# <a name="the-interface-uuid-file"></a>介面 UUID 檔案

介面 UUID 檔會從已處理的 IDL 檔案中的所有介面收集介面識別碼的定義。 類似于存根檔和標頭檔，輸入資料流程關閉是由目前的 IDL 檔案和包含的檔案所定義。 例如，針對介面 IFace，編譯器會產生常數 IID \_ IFace，並將它初始化為 IDL 檔案中指定的介面 UUID。 用戶端應用程式和 proxy DLL 會使用這個常數來識別介面。

從檔案產生之介面 IID 檔案的預設名稱。 .idl 為 File \_ i.c。 [**/Iid**](-iid.md) MIDL 編譯器參數會覆寫介面 UUID 檔案的預設名稱。

 

 




