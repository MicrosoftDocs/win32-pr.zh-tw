---
title: 軟體轉散發
description: 軟體轉散發
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows媒體格式 SDK，軟體轉散發
- Advanced Systems Format (ASF) 、軟體轉散發
- ASF (Advanced Systems Format) ，軟體轉散發
- Windows媒體格式 SDK，轉散發
- Advanced Systems Format (ASF) ，轉散發
- ASF (Advanced Systems Format) ，轉散發
- 軟體轉散發，關於
- 轉散發，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b933df9319c342d8ed3502fc66757df2e6d8fd6e8d60309023ced6ffa042d5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807888"
---
# <a name="software-redistribution"></a>軟體轉散發

在應用程式安裝程式中包含 Windows 媒體格式軟體稱為「轉散發」。 Windows 媒體格式 SDK 包含可包含在應用程式安裝程式中的安裝套件。 安裝套件是名為 wmfdist95.exe 的可執行檔。 當您安裝 Windows 媒體格式 SDK 時，安裝套件會複製到安裝目錄的可轉散發套件 \\ 資料夾， (c： \\ wmsdk \\ wmfsdk 預設為) 。

下列各節提供軟體轉散發設定的程式和其他資訊。



| 區段                                                                            | 描述                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [若要建立轉散發設定](to-create-a-redistribution-setup.md)           | 說明建立應用程式安裝程式的程式。                                                                                                                       |
| [偵測安裝狀態](detecting-setup-status.md)                               | 提供的範例程式碼會檢查登錄中的安裝狀態，以判斷是否需要安裝轉散發套件。                                    |
| [轉散發設定的範例程式碼](example-code-for-redistribution-setup.md) | 提供範例程式碼，可在您的安裝程式常式中用來以無訊息模式執行轉散發套件，並在電腦必須重新開機時通知您的設定常式。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Project考慮**](project-considerations.md)
</dt> </dl>

 

 




