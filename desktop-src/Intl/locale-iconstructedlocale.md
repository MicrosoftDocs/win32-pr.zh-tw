---
description: 地區設定 \_ ICONSTRUCTEDLOCALE 常數描述
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/30/2021
ms.locfileid: "107001248"
---
# <a name="locale_iconstructedlocale"></a>地區設定 \_ ICONSTRUCTEDLOCALE

如果地區設定是「已建立」地區設定，則為要求的識別碼。 不建議使用此 LCTYPE。

這會識別 Windows 上有許多沒有完整資訊的地區設定，而且必須在執行時間「建立」資訊。 一般來說，LOCALE_ICONSTRUCTEDLOCALE 提供的資訊有限，因為 Windows 會提供每個地區設定所能使用的資料量。 因此，不建議使用此 LCTYPE。


| 值 | 意義                 |
|-------|-------------------------|
| 0     | 未結構化         |
| 1     | 是一種結構化的地區設定 |


例如，「de US」或「美國德文」的要求。 NLS 將使用可找到的德文語言資料，以及可找到的美國地區資料。 

這可能不是最理想的，例如，系統可能沒有德文中美國名稱的相關資訊。 但是，如果應用程式或使用者想要「de US」內容，則傳回的資料會是最佳的可用資料。 

使用 LOCALE_ICONSTRUCTEDLOCALE 拒絕地區設定並切換回不同地區設定的應用程式，通常會產生較糟的體驗，例如在此範例中登陸或 en-us。 這兩種方式都不會接近德國語言的原始要求（美國地區）。

