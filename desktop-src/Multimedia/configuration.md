---
title: 'Configuration (Windows 多媒體) '
description: 瞭解 Windows 多媒體驅動程式如何讓使用者藉由顯示 [設定] 對話方塊來選擇設定。
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- 可安裝的驅動程式，設定
- 可安裝的驅動程式，DRV_CONFIGURE 訊息
- DRV_CONFIGURE 訊息
- DRV_QUERYCONFIGURE 訊息
- DRVCONFIGINFO 訊息
- 設定可安裝的驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403921"
---
# <a name="configuration-windows-multimedia"></a>Configuration (Windows 多媒體) 

可安裝的驅動程式可讓使用者在處理 [**Winspool.drv \_ 設定**](drv-configure.md) 訊息時顯示設定對話方塊，以選擇驅動程式和相關聯硬體的設定。 驅動程式負責建立及管理對話方塊、處理對話方塊中的任何使用者輸入，以及變更使用者要求的驅動程式或硬體設定。 驅動程式必須提供個別的對話方塊程式來處理對話方塊的視窗訊息，以及一個對話方塊範本來定義對話方塊的外觀和內容。

接收 WINSPOOL.DRV \_ 設定訊息之前，驅動程式會收到 [**winspool.drv \_ QUERYCONFIGURE**](drv-queryconfigure.md) 訊息。 驅動程式必須傳回非零值給查詢，以確保收到後續 WINSPOOL.DRV \_ 設定訊息。

初始化設定對話方塊時，驅動程式通常會從登錄中抓取設定資訊。 為了協助找出這項資訊，WINSPOOL.DRV \_ 設定訊息通常會包含 [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) 結構的位址，其中包含與驅動程式相關聯的登錄機碼和值的名稱。 如果使用者要求變更設定，驅動程式應該會更新登錄中的設定資訊。

 

 
