---
description: 使用者可以指定印表機的預設檔設定。 這稱為每一使用者的 DEVMODE，因為它只會影響特定使用者的預設值，而每個印表機的資訊會定義在不同的 DEVMODE 結構中。
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5e9fd2872d055dba6d04f060e6d2e581e461fd20ddc418f643d09170cda31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731921"
---
# <a name="per-user-devmode"></a>Per-User DEVMODE

使用者可以指定印表機的預設檔設定。 這稱為每一 *使用者的 DEVMODE* ，因為它只會影響特定使用者的預設值，而每個印表機的資訊會定義在不同的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構中。

若要設定每位使用者的 DEVMODE，請使用 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)或 [**印表機 \_ 資訊 \_ 9**](printer-info-9.md)結構來呼叫 [**SetPrinter**](setprinter.md) 。 若要將每位使用者的 DEVMODE 重設為全域預設的 [**devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)，請使用 [**印表機 \_ 資訊 \_ 8**](printer-info-8.md)結構來呼叫 **SetPrinter** 。

 

 



