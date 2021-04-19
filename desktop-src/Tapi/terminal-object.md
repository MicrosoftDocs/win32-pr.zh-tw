---
description: 在 TAPI 3.0 版和更新版本中，TAPI 物件模型會使用終端物件來代表與通話或通訊會話相關聯之媒體資料流程的來源或接收。
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Terminal 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2568d3c6f047fec8ca46b3b7d56e5026b61a1113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990500"
---
# <a name="terminal-object"></a>Terminal 物件

在 TAPI 3.0 版和更新版本中，TAPI 物件模型會使用終端物件來代表與通話或通訊會話相關聯之媒體資料流程的來源或接收。 此物件模型可讓應用程式在詳細層級指定媒體在呼叫上的處理方式。 此模型也可同時選取多個終端機，例如，呼叫可以輸出到音訊喇叭並同時錄製。

終端物件代表來源或轉譯器，例如麥克風或喇叭。 應用程式會根據與通訊會話相關的媒體方向和類型或類型，從可用的終端機中選擇。 接著，每個相關聯的媒體串流都會選取到適當的終端機，以便開始串流。

終端機通常由媒體服務提供者（ () MSP）來執行，如果沒有與通訊會話相關聯的 MSP，終端機物件將無法使用。 其中一個例外狀況是在 Windows 2000 SP1 和更新版本中，應用程式可以執行一種可 [插入的終端](pluggable-terminals.md)機形式。 這可讓會議服務器建立橋接終端機，以便將非 Windows 2000 SP1 或非多播 H323 用戶端新增至 TAPI 3 多方的 SDP/IP 多播會議。

每個終端機都屬於一個 [終端機類別](terminal-class.md)。 終端機類別代表一組來源或轉譯功能。 例如，對應至一組音訊喇叭的終端機會被視為 CLSID \_ SpeakersTerminal，而服務提供者預期會執行磁片區控制。 TAPI 3 會定義一組終端機類別、MSP 可以定義額外的類別，而應用程式可註冊新的終端機類別。 每個終端機類別都會被指派全域唯一識別碼 (GUID) 。

從應用程式的觀點來看，終端機會依其 [終端機類型](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) 和 [方向](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)來描述。 此類型可以是靜態或動態。 靜態終端機會對應到硬體，例如電話或麥克風。 動態終端機會對應至暫時性物件，例如檔案或影片視窗。 方向描述給定的終端機是否為來源或轉譯器。

給定終端物件的功能可能會根據目前使用中的服務提供者組而有很大的差異。 特殊化裝置的 MSP 可能會使用適合該裝置的方法來執行介面。 該介面可以匯總到終端機物件上，並讓應用程式可以使用方法。 如需詳細資訊和參考資料，請參閱媒體服務提供者檔。

如需有關 TAPI 3 所執行之終端介面和方法的詳細資訊，請參閱 [終端物件介面](terminal-object-interfaces.md)。

如果媒體服務提供者的作者使用 MSP 基類，它們可能會執行部分媒體串流處理終端機功能。

如需顯示使用終端機物件圖例的詳細資訊和程式碼範例，請參閱 [進行呼叫](make-a-call.md) 和 [接收呼叫](receive-a-call.md)。

**WINDOWS XP：** 如需有關如何在 Windows XP 中展開終端機物件的詳細資訊，請參閱檔案 [終端](file-terminals.md)機、 [Multitrack 終端](multitrack-terminals.md)機和可 [插入的終端](pluggable-terminals.md)機。

如需詳細資訊和程式碼範例，請參閱 [使用檔案終端](using-file-terminals.md)機、 [使用 Multitrack 終端機和預設選取機制](using-multitrack-terminals-and-the-default-selection-mechanism.md)，以及 [插入式終端機註冊](pluggable-terminal-registration.md)。

 

 



