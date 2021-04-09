---
title: Network List Manager 的角色
description: Network List Manager 的角色
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840824"
---
# <a name="the-role-of-network-list-manager"></a>Network List Manager 的角色

在 Windows XP 與 Windows Server 2003 之前，應用程式必須呼叫一些不相關的 Api，以取得網路屬性的相關資料，例如 IP 位址、網域控制站或網域名稱系統 (DNS) 。 從 Windows XP 和 Windows Server 2003 開始，網路定位感知 Winsock API 會提供一組有限的網路位置功能。 在 Windows Server 2008 和 Windows Vista 中，網路覺察服務會在一個位置中捕捉網路屬性，並讓應用程式查詢及取出特定的網路和屬性。 網路清單管理員會以 Winsock 命名空間提供者取代舊版 Winsock API (的功能，) 同時使用 Winsock API 維持與繼承應用程式的相容性。

 

 




