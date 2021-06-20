---
description: 瞭解擴充性。 布建是以與裝置無關的方式和裝置特定的方式來擴充常數和結構。
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: " (電話語音 API) 的擴充性"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f29ad34b5156bdd652ab6b6f8901be7a2341bdc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406561"
---
# <a name="extensibility"></a>擴充性

布建是以與裝置無關的方式，以及裝置特定的 (廠商特定) 方式來擴充常數和結構。 在純量列舉的常數中，會保留值範圍，供未來的一般延伸模組使用。 其餘的值會識別為裝置特定。 廠商可以用任何想要的方式來定義這些值的意義。 其轉譯會以 [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)資料結構中所提供的 *延伸模組識別碼* 做為索引鍵。 針對定義為位旗標的常數，會保留低序位位範圍，其中高序位位可以是擴充功能的特定範圍。 建議將擴充值和位陣列使用最高值或高序位位的位。 如果未來需要這樣做，則可以選擇在一般部分和延伸部分之間移動框線。 資料結構的延伸會被指派大小可變大小的欄位，其中大小/位移是固定部分的一部分。 TAPI 會針對每個資料結構描述允許的裝置特定延伸模組。

除了辨識特定的延伸模組識別碼之外，應用程式也必須協調應用程式和服務提供者在其下運作的延伸模組版本號碼。 這是在 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) 函式的第二個版本協商階段中完成。

延伸模組識別碼是全域唯一的識別碼。 延伸模組識別碼沒有中央登錄。 相反地，它們是由工具組在本機由工具組提供的公用程式所產生。 此數位是由各部分組成，例如唯一的 LAN 位址、一天中的時間和亂數字，以保證全域唯一性。 全域唯一識別碼的設計目的是要與 HP/DEC 通用唯一識別碼區別，因此完全與其相容。

 

 
