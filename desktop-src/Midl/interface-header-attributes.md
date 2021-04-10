---
title: 介面標頭屬性
description: 將這些屬性併入介面標頭中，以傳達整個介面的相關資訊。
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL、屬性、介面標頭
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021254"
---
# <a name="interface-header-attributes"></a>介面標頭屬性

將這些屬性併入介面標頭中，以傳達整個介面的相關資訊。



| 屬性                                   | 使用方式                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**非同步 \_ uuid**](async-uuid.md)           | 指示 MIDL 編譯器定義 COM 介面的同步和非同步版本。                                                                                                                                               |
| [**uuid**](uuid.md)                        | 指定可區分特定介面與其他介面的128位值。 實際值可能代表 GUID、CLSID 或 IID。                                                                                                 |
| [**當地**](local.md)                      | 指示 MIDL 編譯器只產生標頭檔。 介面必須有 [**uuid**](uuid.md) 或 [**區域**](local.md) 屬性。                                                                                             |
| [**ms 聯 \_ 集**](-ms-union.md)              | 控制 nonencapsulated 聯集的 NDR 對齊。 用於回溯相容性與以 MIDL 1.0 或2.0 為基礎的介面。                                                                                                                   |
| [**物件**](object.md)                    | 將介面識別為 COM 介面，並指示 MIDL 編譯器產生 proxy/stub 程式碼，而不是 RPC 用戶端和伺服器 stub。                                                                                                    |
| [**版本**](version.md)                  | 識別介面的多個版本存在時的特定版本。 因為 COM 介面是不可變的，所以您無法在 [**物件**](object.md)介面上使用 [**version**](version.md)屬性。 |
| [**指標 \_ 預設值**](pointer-default.md) | 指定所有指標的預設指標類型，但參數清單中包含的指標除外。 預設類型可以是 [**unique**](unique.md)、 [**ref**](ref.md)或 [**ptr**](ptr.md)。                                                   |
| [**端點**](endpoint.md)                | 指定伺服器應用程式將接聽遠端程序呼叫的靜態 (已知) 端點。                                                                                                                                   |



 

請參閱程式庫語句內所定義或參考之介面屬性的 [類型程式庫屬性](type-library-attributes.md) （例如 [**雙重**](dual.md) 和 [**oleautomation**](oleautomation.md)）。

 

 




