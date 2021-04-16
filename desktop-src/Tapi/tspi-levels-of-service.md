---
description: TAPI 將通訊服務分成基本、補充和延伸。 如需其他資訊，請參閱 TAPI 的服務層級。
ms.assetid: e2e6b113-b6b0-43a1-ac95-6e8e188a6120
title: TSPI 服務層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d829199bdcfce350d82f3c56cbbf9414fc46b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513468"
---
# <a name="tspi-levels-of-service"></a>TSPI 服務層級

TAPI 將通訊服務分成基本、補充和延伸。 如需其他資訊，請參閱 [TAPI 的服務層級](./tapi-levels-of-service.md) 。

必須有 TSP，才能執行所有基本的電話語音功能。 [TSPI 基本電話語音功能](tspi-basic-telephony-functions.md) 包含這些功能的摘要。

補充電話語音包含新式 Pbx 上的功能，例如保存、傳輸、會議、公園等等。 服務提供者應該只有在可執行 TAPI 所定義的確切意義時，才提供補充的電話語音服務。 如果沒有，則應以擴充電話語音服務的形式提供此功能。 所有補充功能都是選擇性的。 服務提供者會透過回應（例如 [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) 或 [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)），指定其所支援的服務。 單一補充服務可以包含多個函式呼叫和訊息。 電話裝置服務是補充電話語音的一部分。

擴充的電話語音服務允許提供者執行裝置特定的功能。 服務提供者必須使用 *延伸模組識別碼* 來唯一識別延伸。 應用程式會取出並使用這個唯一識別碼來判斷服務提供者所支援的延伸模組。

這些延伸模組可適用于數個製造商。 TAPI 提供特殊的功能和訊息，例如 [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) 和 [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) 。 它們可用來讓函數集的擴充功能 (與服務提供者所支援) 的列舉、位旗標和資料結構成員不同。 每個函式的參數也會由服務提供者定義。

在散發) 之前，會將識別碼指派給一組延伸 (，而不是指派給這些擴充功能的每個個別實例。 TSPI 中的 EXTIDGEN 公用程式會為服務提供者產生唯一的延伸模組識別碼。 它會使用乙太網路介面卡位址、亂數字和一天中的時間來產生識別碼，因此，產生的延伸模組識別碼不太可能會與任何其他服務提供者發生衝突。 因此，廠商不需要註冊延伸模組識別碼。

除非執行電腦的電腦也正在執行 NetBIOS 或其他網路軟體，否則 EXTIDGEN 公用程式不會產生延伸模組識別碼。

 

 
