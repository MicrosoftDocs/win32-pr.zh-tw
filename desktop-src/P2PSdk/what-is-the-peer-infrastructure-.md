---
description: 對等基礎結構是一組功能強大且有彈性的 Api。
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: 什麼是對等基礎結構？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e80a5cdcc190fe47ea0a37efd5348ec5f718eaff654543c68bd6e9d355d4d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119287638"
---
# <a name="what-is-the-peer-infrastructure"></a>什麼是對等基礎結構？

對等基礎結構是一組功能強大且有彈性的 Api。 主要的元件包括下列各項：

-   [對等圖形 API](#peer-graphing-api)
-   [對等群組 API](#peer-grouping-api)
-   [對等身分識別管理員 API](#peer-identity-manager-api)
-   [PNRP 命名空間提供者 API](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>對等圖形 API

對等基礎結構提供圖形技術，可在對等圖形中的對等之間有效率且可靠地傳遞資訊。 [對等圖形 API](graphing-api.md)可確保每個節點在圖形中都具有一致的資料檢視。

您可以使用 [對等圖形 API](graphing-api.md) 來執行下列動作：

-   建立和管理對等圖形
-   列舉對等圖形中的其他對等，並與之互動
-   以 a [記錄](records.md) 的形式將資料傳送至對等圖形中的每個節點

## <a name="peer-grouping-api"></a>對等群組 API

[對等群組 API](grouping-api.md)結合和增強對等[PNRP](#pnrp-namespace-provider-api)和[圖形](#peer-graphing-api)api，並新增下列兩個元件：

-   多工層，可讓一個對等實體上執行的多個應用程式連接到群組
-   一種特定的安全性模型，可確保只有受邀加入群組的對等，才能在群組的存留期內連接到群組

您可以使用對等群組 API 來執行下列動作：

-   建立和管理安全對等群組
-   列舉群組中的其他對等，並與之互動
-   以 a [記錄](records.md) 的形式將資料傳送至對等群組中的每個節點

## <a name="peer-identity-manager-api"></a>對等身分識別管理員 API

您可以使用 [對等身分識別管理員 API](identity-manager-api.md) 建立安全的 [對等名稱](peer-names.md) ，以供 PNRP 用來確保發佈名稱的使用者正式擁有名稱。 對等名稱也稱為身分識別，並會在對等群組 API 中用來識別群組中的個人。

您可以使用 [對等身分識別管理員 API](identity-manager-api.md) 來執行下列動作：

-   建立、列舉和管理對等身分識別。

## <a name="pnrp-namespace-provider-api"></a>PNRP 命名空間提供者 API

對等基礎結構提供無伺服器名稱解析技術，稱為 [PNRP 命名空間提供者 API](pnrp-namespace-provider-api.md)。 藉由使用 Winsock 2 PNRP 命名空間提供者 API，對等、服務、計算裝置和對等群組端點可以管理、註冊、取消註冊和解析 PNRP [雲端](clouds.md)中的另一個端點。

> [!Note]  
> PNRP 是 **對等名稱解析通訊協定** 的縮寫。

 

 

 



