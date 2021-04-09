---
title: Server-Side 記錄
description: 伺服器端記錄可在 URL 群組或伺服器會話上取得。
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840376"
---
# <a name="server-side-logging"></a>Server-Side 記錄

伺服器端記錄可在 URL 群組或伺服器會話上取得。 當伺服器會話啟用記錄功能時，它會以集中式形式記錄伺服器會話下的所有 URL 群組。 在 URL 群組上啟用記錄功能時，只會在路由至 URL 群組的要求上執行記錄。 HTTP 伺服器 API 支援下列記錄類型：

-   [W3C 記錄](w3c-logging.md)：適用于伺服器會話和 URL 群組。
-   [NCSA 記錄](ncsa-logging.md)：可在 URL 群組上使用。
-   [IIS 記錄](iis-logging.md)：可在 URL 群組上使用。
-   [集中式二進位記錄](centralized-binary-logging.md)：適用于伺服器會話。

為了利用 HTTP 記錄功能，應用程式會在伺服器會話或 URL 群組上啟用及設定一種記錄。 如需詳細資訊，請參閱設定 [和啟用伺服器端記錄](configuring-and-enabling-server-side-logging.md)

 

 




