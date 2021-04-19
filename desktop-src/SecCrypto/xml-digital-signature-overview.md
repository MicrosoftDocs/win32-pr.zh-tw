---
description: XML 是描述結構化資料的業界標準。 XML 數位簽章是數位簽章的 XML 標記法，可讓您驗證 XML 檔和外部參考資料的來源和完整性。
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: XML 數位簽章總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001378"
---
# <a name="xml-digital-signature-overview"></a>XML 數位簽章總覽

XML 是描述結構化資料的業界標準。 XML 數位簽章是 [*數位簽章*](../secgloss/d-gly.md) 的 xml 標記法，可讓您驗證 XML 檔和外部參考資料的來源和完整性。 XML 數位簽章可以用來簽署任意資料，包括 XML 檔或片段、HTML 網頁、純文字或二進位編碼的資料（例如 JPEG 檔案）。

CryptXML 數位簽章 API 所支援的 XML 數位簽章格式是由 XML 簽章語法和處理 (第二版) W3C 建議所指定。

CryptXML 數位簽章可支援所需的簽章類型、密碼編譯演算法、正常化演算法和指定的封包轉換。

開發人員可以藉由建立密碼編譯延伸模組 Dll，來擴充 CryptXML 所支援的一組預設密碼編譯演算法。 開發人員也可以在 CryptXML API 之上建立自己的自訂轉換和標準化演算法。 開發人員可以使用 CryptXML Api 搭配 Windows 憑證 Api。

 

 
