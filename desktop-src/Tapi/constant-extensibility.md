---
description: 布建是以與裝置無關的方式，以及裝置特定的 (廠商特定) 方式來擴充常數和結構。
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: 常數延伸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a470ccb52af1bdc92596ac42bbafb74d4821db1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971450"
---
# <a name="constant-extensibility"></a>常數延伸

布建是以與裝置無關的方式，以及裝置特定的 (廠商特定) 方式來擴充常數和結構。

在純量列舉的常數中，會保留值範圍，供未來的一般延伸模組使用。 其餘的值會識別為裝置特定。 廠商可以用任何想要的方式來定義這些值的意義。 這些值的解讀會以透過 [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) 資料結構所提供的延伸模組識別碼做為索引鍵。 針對定義為位旗標的常數，會保留低序位位範圍，其中高序位位可以是擴充功能的特定範圍。 建議將擴充值和位陣列使用最高值或高序位位的位。 如果未來需要的話，這會讓您在一般部分和延伸部分之間移動框線。 資料結構的延伸會被指派大小可變大小的欄位，其中大小/位移是固定部分的一部分。 TSPI 說明每個資料結構允許的裝置特定延伸模組。 如需詳細資訊，請參閱 [記憶體配置](./memory-allocation.md) 主題。

除了辨識特定的延伸模組識別碼之外，TAPI (可以代表應用程式運作) 必須協調應用程式和服務提供者將在其下運作的延伸模組版本號碼。 這是使用 [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) 和 [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) 函數來完成。

延伸模組識別碼是全域唯一的識別碼。 延伸模組識別碼沒有中央登錄。 相反地，它們是由工具組在本機由工具組提供的公用程式所產生。 為了保證全域唯一性，數位是由 (唯一) LAN 位址、一天中的時間和亂數字等元件組成。 全域唯一識別碼的設計目的是要與 HP/DEC 通用唯一識別碼區別，因此完全與其相容。

 

 
