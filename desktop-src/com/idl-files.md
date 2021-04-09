---
title: IDL 檔案
description: IDL 檔案
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842780"
---
# <a name="idl-files"></a>IDL 檔案

COM 使用 Microsoft 介面定義語言 (MIDL) 來描述 COM 物件。 MIDL 是開放式 Software Foundation 所定義之分散式運算環境的 IDL 延伸模組，其開發目的是要針對傳統用戶端/伺服器應用程式中的遠端程序呼叫定義介面。 MIDL 包含物件定義語言的大部分屬性和語句 (ODL) ，這是原本用來產生 OLE Automation 型別程式庫的語言。

在 c + + 和 JAVA 中，建立 COM 物件的開發人員會建立一個 IDL 檔案，MIDL 編譯器接著會處理該檔案，以建立類型程式庫或標頭和 proxy 檔案，或兩者。 *類型程式庫* 是描述 com 物件或 com 介面的二進位檔案，或兩者。 類型程式庫是 IDL 檔案的編譯版本。 不過，類型程式庫只支援 ODL 語義。 尤其是，它們無法表示與 IDL 屬性相關的 IDL 檔案中的所有資訊，例如 \[ [**大小 \_**](/windows/desktop/Midl/size-is) \] 。 您必須針對在類型程式庫中遺失資訊的 IDL 檔案，建立和使用 proxy 檔案。

在 Visual Basic 中，建立 COM 物件的開發人員不會建立 IDL 檔案。 相反地，Visual Basic 會使用類別和專案屬性來收集資訊，並直接建立類型程式庫。

 

 