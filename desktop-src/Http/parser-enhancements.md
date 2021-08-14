---
title: 剖析器增強功能
description: 剖析器增強功能
ms.assetid: b520aebe-9182-4e60-9111-49af09cdbd79
keywords:
- 剖析器增強功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff184fc978865f3e76dbcc24f9c628b3b3f42c2bc286c4854247b0c4b4c4b59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393871"
---
# <a name="parser-enhancements"></a>剖析器增強功能

在 Windows server 2003 （含 Service Pack 1） (SP1) 中，HTTP 伺服器 API 允許來自 HTTP 用戶端的下列要求。

-   使用單行換行 (LF) 為行結束字元的要求。
-   包含線性泛空白字元的要求 (LWS 在 HTTP 要求行與標頭開頭之間) 。

預設會啟用這些行為，而且不受登錄設定控制。

 

 




