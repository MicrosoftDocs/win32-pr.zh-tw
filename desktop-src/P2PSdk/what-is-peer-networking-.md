---
description: 對等網路是一種無伺服器的網路技術，可讓數個網路裝置共用資源，並直接彼此通訊。
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: 什麼是對等網路？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c456fac9b7695a2846765ee0ccd38c1e5df646e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944272"
---
# <a name="what-is-peer-networking"></a>什麼是對等網路？

對等網路是一種無伺服器的網路技術，可讓數個網路裝置共用資源，並直接彼此通訊。 這項技術適用于 Windows XP Service Pack 1 (SP1) 和更新版本的用戶端，這些用戶端會執行適用于對等基礎結構的 Advanced 網路套件。

對等基礎結構是一組網路 Api，可協助您開發使用網路上電腦之共同功能的非集中式網路應用程式。 例如，對等應用程式可以是共同作業通訊、內容發佈技術等等。

對等基礎結構提供穩固的網路基礎結構，讓您可以專注于開發應用程式，因為基礎結構是為您而開發。

對等基礎結構包含下列主要元件：

-   [可擴充且安全的對等名稱解析](#scalable-and-secure-peer-name-resolution)
-   [有效的 multipoint 通訊](#efficient-multipoint-communication)
-   [分散式資料管理](#distributed-data-management)
-   [安全對等身分識別](#secure-peer-identities)
-   [安全對等群組](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>可擴充且安全的對等名稱解析

[對等名稱解析通訊協定 (PNRP) 命名空間提供者 API](pnrp-namespace-provider-api.md)是一種名稱對 IP 解析通訊協定。 包含所有參與對等的 IPv6 範圍或內容稱為 [雲端](clouds.md)。 PNRP 可讓對等在雲端內彼此互動。

## <a name="efficient-multipoint-communication"></a>有效的 Multipoint 通訊

對等基礎結構包含可提供有效 multipoint 通訊的 [圖形 API](graphing-api.md) 。 如同 PNRP，點對點圖形可讓一組節點進行互動，並以 [記錄](records.md)的形式互相傳遞資料。 對等產生或更新的每一筆記錄都會傳送到圖形中的所有節點。

## <a name="distributed-data-management"></a>分散式資料管理

分散式資料管理會自動儲存所有傳送至對等圖形的記錄，直到每筆記錄的指定到期時間為止。 對等網路可確保點對點圖形中的每個節點都具有記錄資料庫的類似觀點。 如果對等圖形具有與其相關聯的安全性模型，則圖形會包含下列資訊：

-   誰可以和無法連接至圖形
-   誰可以根據外部定義的準則來保護和驗證記錄

## <a name="secure-peer-identities"></a>安全對等身分識別

對等的基礎結構提供對等身分 [識別管理員 API](identity-manager-api.md) ，可讓您建立、管理和操作對等身分識別。 對等身分識別是用來定義 PNRP 中安全端點的名稱，而且可以代表任何參與對等網路的資源，包括安全的對等群組和服務。

## <a name="secure-peer-to-peer-groups"></a>安全對等群組

對等 [群組 API](grouping-api.md) 結合了對等圖形、Identity MANAGER 和 PNRP api，形成對等網路應用程式開發的一致且方便的解決方案。 點對點群組 API 會使用對等身分識別管理員 API 和自我簽署憑證配置，以確保圖形基礎結構內的安全性。 您可以透過 PNRP 解析和註冊每個群組，以允許在註冊的點對點群組內進行隨機對等的名稱解析。 群組可以是 PNRP 中的端點，就像對等一樣。

如需對等基礎結構的總覽，請參閱「[WINDOWS XP 對等網路簡介](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)」一文。

如需對等基礎結構中的 Api 總覽，請參閱「 [什麼是對等基礎結構？](what-is-the-peer-infrastructure-.md)」主題。

 

 



