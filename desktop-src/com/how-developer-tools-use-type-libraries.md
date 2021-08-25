---
title: 開發人員工具如何使用類型程式庫
description: 開發人員工具如何使用類型程式庫
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e829459176d96beab3fd818b7bafe3cddfb7969ff46531d26709ef6391ecc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993070"
---
# <a name="how-developer-tools-use-type-libraries"></a>開發人員工具如何使用類型程式庫

下圖說明各種開發工具如何與 COM 物件的類型程式庫互動。 每個類型程式庫會公開標準的程式設計介面，工具可以呼叫這些介面來取得該類型程式庫中所述專案的相關資訊。 在此圖中，GUID 代表遠端程序呼叫的全域唯一識別碼和 RPC。

![顯示開發只有才如何與 C O M 物件的類型程式庫互動的圖表。](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

在上圖中，c + + 轉換工具，例如 MIDL 編譯器和 Microsoft Visual C++ 開發系統提供的嚮導，會產生標頭和存根檔案。 您可以將這些檔案新增至您的專案，以便使用類型程式庫所描述的 COM 物件。

同樣地，在 JAVA 中，開發人員工具會產生 JAVA 類別和原始程式檔，然後您就可以將其匯入至應用程式。

在 Visual Basic 中，此案例稍微簡單許多。 您不需要產生其他檔案。 Visual Basic 環境會提供對話方塊，列出目前安裝在電腦上的 COM 物件。 您可以從應用程式中選取要呼叫的元件，並將它新增至您的專案，以做為元件或參考。

OLE COM 檢視器會讀取類型程式庫、根據類型程式庫產生暫時性的 IDL 檔案，然後將它顯示給使用者。 OLE COM 檢視器也會顯示類型程式庫中所列 COM 元素的 c + + 語法。

如需型別程式庫的詳細資訊，請參閱 [類型程式庫和物件描述語言](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language)。

 

 