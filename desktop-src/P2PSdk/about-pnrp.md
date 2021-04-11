---
description: 對等名稱解析通訊協定 (PNRP) 命名空間提供者 (NSP) 是無伺服器名稱解析技術，可讓節點彼此探索。
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: 關於 PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115585"
---
# <a name="about-pnrp"></a>關於 PNRP

對等名稱解析通訊協定 (PNRP) 命名空間提供者 (NSP) 是無伺服器名稱解析技術，可讓節點彼此探索。 PNRP 使用 Winsock 2 命名空間提供者 API。

PNRP 需要 IPv6 支援，而且是唯一的 API 原生網際網路通訊協定。 不過，PNRP 可以透過6to4 或 [Teredo](/windows/desktop/Teredo/portal) 轉換技術來解析 IPv4 位址。 Windows XP Service Pack 1 (SP1) 使用者必須下載 [Advanced 網路套件](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) ，才能啟用 PNRP 所需的 IPv6 支援。

> [!Note]  
> 在具有防火牆的環境中使用 PNRP 的應用程式需要例外狀況群組，其中涵蓋應用程式特定的埠，以及 PNRP 的埠 ' 3540-UDP '。 每當應用程式執行時，都應啟用這些例外狀況群組。

 

雖然 PNRP 2.0 對 Windows Vista 和 Windows Server 2008 平臺而言是原生的，但 Windows XP 使用者必須下載 Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) ，才能升級至 PNRP 2.0。

 

 
