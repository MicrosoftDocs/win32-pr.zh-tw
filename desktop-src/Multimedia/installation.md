---
title: '安裝 (Windows 多媒體) '
description: 瞭解 Windows 多媒體安裝，包括處理 DRV_INSTALL 和 DRV_REMOVE 訊息。
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- 可安裝的驅動程式，安裝
- 可安裝的驅動程式，DRV_INSTALL 訊息
- 可安裝的驅動程式，DRV_REMOVE 訊息
- DRV_INSTALL 訊息
- DRV_REMOVE 訊息
- DRVCONFIGINFO 訊息
- 安裝驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01ef47952f3d5a62c0dce246bf24689d37f11326f0f3ec251f7afc19c822fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140676"
---
# <a name="installation-windows-multimedia"></a>安裝 (Windows 多媒體) 

可安裝的驅動程式可以在處理 [**Winspool.drv \_ 安裝**](drv-install.md) 和 [**winspool.drv \_ 移除**](drv-remove.md) 訊息時，執行驅動程式特定的安裝工作。 安裝或移除驅動程式時，安裝應用程式（例如主控台應用程式）會將訊息傳送至驅動程式。

處理 WINSPOOL.DRV \_ 安裝訊息時，驅動程式通常會確認所需的硬體存在，然後顯示 [設定] 對話方塊，讓使用者選擇驅動程式和相關聯硬體的初始設定。 訊息包含 [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) 結構的位址，其中包含與驅動程式相關聯的登錄機碼和值的名稱。驅動程式會檢查登錄值以取得預設的設定資訊。 最後，驅動程式也會建立成功操作所需的任何其他登錄機碼和值。

處理 WINSPOOL.DRV \_ 移除訊息時，驅動程式會移除任何可能已建立的登錄機碼和值。

 

 
