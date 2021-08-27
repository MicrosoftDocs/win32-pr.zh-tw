---
title: 查詢輔助音訊裝置
description: 查詢輔助音訊裝置
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- 波形音訊，查詢輔助音訊裝置
- 輔助音訊，查詢裝置
- 輔助音訊介面
- 輔助音訊裝置，查詢
- 查詢輔助音訊裝置
- 輔助音訊、介面
- 輔助音訊、裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a6d61634475c3b921428529df69113c921b8c5bff8d1a65d5b08931a670fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037568"
---
# <a name="querying-auxiliary-audio-devices"></a>查詢輔助音訊裝置

並非所有的多媒體系統都有輔助的音訊支援。 您可以使用 [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) 函式來判斷系統中有可控制的輔助裝置數目。

若要取得特定輔助音訊裝置的相關資訊，請使用 [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) 函數。 此函式會以指定裝置功能的相關資訊填入 [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) 結構。 此資訊包含製造商和產品識別碼、裝置的產品名稱，以及裝置驅動程式版本號碼。

 

 