---
description: 布建是以與裝置無關的方式，以及裝置特定的 (廠商特定) 方式來擴充常數和結構。
ms.assetid: d30f80c3-3535-4d78-b0a1-c9a7389f8fd4
title: 結構擴充性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fcf80b1ecfb7cc4d31b9ff040b101707ae236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978176"
---
# <a name="structure-extensibility"></a>結構擴充性

布建是以與裝置無關的方式，以及裝置特定的 (廠商特定) 方式來擴充常數和結構。

在純量列舉的常數中，會保留值範圍，供未來的一般延伸模組使用。 其餘的值會識別為裝置特定。 廠商可以用任何方式定義這些值的意義。 這些值的解讀會以 [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)資料結構所提供的 *延伸模組識別碼* 做為索引鍵。 針對定義為位旗標的常數，會保留低序位位範圍，其中高序位位可以是擴充功能的特定範圍。 建議將擴充值和位陣列使用最高值或高序位位的位。 如果未來需要這樣做，則可以選擇在一般部分和延伸部分之間移動框線。 資料結構的延伸會被指派大小可變大小的欄位，其中大小/位移是固定部分的一部分。 TSPI 會針對每個資料結構描述允許的裝置特定延伸模組。

除了辨識特定的延伸模組識別碼之外，TAPI (可以代表應用程式運作) 必須協調應用程式和服務提供者運作的延伸模組版本號碼。 這是使用 [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) 和 [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) 函數來完成。

延伸模組識別碼是全域唯一的識別碼。 延伸模組識別碼沒有中央登錄。 相反地，它們是由工具組在本機由工具組提供的公用程式所產生。 此數位是由各部分組成，例如 (唯一) LAN 位址、一天中的時間和亂數字，以保證全域唯一性。 全域唯一識別碼的設計目的是要與 HP/DEC 通用唯一識別碼區別，因此完全與其相容。

 

 
