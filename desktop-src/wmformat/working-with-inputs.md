---
title: 使用輸入
description: 使用輸入
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media Format SDK，使用輸入
- Advanced Systems Format (ASF) ，使用輸入
- ASF (Advanced Systems Format) ，使用輸入
- 設定檔，使用輸入
- 資料流程，使用輸入
- 編解碼器，使用輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462144"
---
# <a name="working-with-inputs"></a>使用輸入

就像設定檔中的適當串流設定需要取得編解碼器來壓縮資料流程一樣，您也必須確定您傳遞給寫入器的未壓縮媒體類型已正確描述。 每個 Windows Media 編解碼器都有相關聯的預設輸入類型，但支援數種輸入類型。 您可以檢查支援的輸入，並選取符合您資料的輸入。 使用輸入的程式會在下列步驟中摘要說明：

1.  當您載入要使用之寫入器的設定檔時，寫入器物件會為設定檔中的每個連接指派輸入編號。 如需載入寫入器設定檔的詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。 除非您使用依位速率的互斥，否則每個串流都有一個連接。 位元速率互斥的資料流程會共用單一連接。
2.  您的應用程式應該識別檔案的輸入編號。 如需識別輸入數位的詳細資訊，請參閱 [以數位識別](to-identify-inputs-by-number.md)輸入。
3.  針對每個輸入，您應該確保輸入格式符合您的資料。 您可以列舉 SDK 所支援的輸入格式。 如需詳細資訊，請參閱 [來列舉輸入格式](to-enumerate-input-formats.md)。 您無法列舉已壓縮之任意資料流程或資料流程的輸入格式。 如需這些特殊案例的詳細資訊，請參閱 [任意和 Precompressed 的資料流程輸入](arbitrary-and-precompressed-stream-inputs.md)。
4.  為每個連接指派正確的輸入格式。 如需詳細資訊，請參閱 [指派輸入格式](assigning-input-formats.md)。
5.  某些編解碼器和寫入器功能是在編碼時間進行設定，而不是在設定檔中設定。 若要設定這些功能，您必須使用輸入設定。 如需詳細資訊，請參閱 [設定輸入](to-set-input-settings.md)設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




