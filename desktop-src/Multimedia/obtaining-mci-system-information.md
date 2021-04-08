---
title: 取得 MCI 系統資訊
description: 取得 MCI 系統資訊
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932116"
---
# <a name="obtaining-mci-system-information"></a>取得 MCI 系統資訊

[Sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) 命令會取得有關 MCI 裝置的系統資訊。 MCI 會處理此命令，而不將它轉送到任何 MCI 裝置。 針對命令訊息介面，MCI 會傳回 [**mci \_ SYSINFO \_ PARMS**](mci-sysinfo-parms.md) 結構中的系統資訊。

您可以使用 **sysinfo** (MCI \_ sysinfo) 命令來取得資訊，例如系統上的 mci 裝置數目、特定類型的 mci 裝置數目、開啟的 MCI 裝置數目，以及裝置的名稱。 此命令通常會被呼叫一次以上，以抓取特定的資訊片段。 例如，您可能會在第一次呼叫中取得特定類型的裝置數目，然後在下一步列舉裝置的名稱。

 

 




