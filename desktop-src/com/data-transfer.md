---
title: 資料轉送
description: 資料轉送
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98e7f546cab245e1f2d2d06036379ea5b28526edcf42aa8a364ea04688db034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993484"
---
# <a name="data-transfer"></a>資料轉送

元件物件模型 (COM) 提供在應用程式之間傳輸資料的標準機制。 這項機制是 *資料物件*，只是任何會實 [**IDATAOBJECT**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面的 COM 物件。 某些資料物件（例如複製到剪貼簿的文字片段）具有 **IDataObject** 做為其唯一介面。 有些則會公開多個介面，例如複合檔案物件， **IDataObject** 只是一個。 資料物件是使用複合檔案的基礎，雖然它們在該 OLE 技術之外也有廣泛的應用程式。

藉由交換資料物件的指標，資料的提供者和取用者就能以一致的方式管理資料傳輸，不論資料格式為何、用來傳送資料的媒體類型，或是要轉譯的目標裝置。 您可以在應用程式中包含基本剪貼簿傳輸的支援、拖放傳輸，以及使用單一 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)執行的 OLE 複合檔案傳輸。 這麼做之後，需要用來容納每個通訊協定之特殊語義的程式碼數量很少。

如需詳細資訊，請參閱下列主題：

-   [資料傳輸介面](data-transfer-interfaces.md)
-   [資料格式和傳輸媒體](data-formats-and-transfer-media.md)
-   [拖放功能](drag-and-drop.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複合檔案](compound-documents.md)
</dt> </dl>

 

 




