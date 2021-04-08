---
title: WinRM 外掛程式 API
description: " (API) 的 WinRM 外掛程式應用程式開發介面所提供的功能，可讓使用者藉由針對支援的資源 Uri 和作業來執行某些 Api 來寫入外掛程式。"
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932371"
---
# <a name="winrm-plug-in-api"></a>WinRM 外掛程式 API

Windows 遠端管理外掛程式是原生動態連結程式庫 (Dll) ，可插入和擴充 WinRM 的功能。  (API) 的 WinRM 外掛程式應用程式開發介面所提供的功能，可讓使用者藉由針對支援的 [*資源 uri*](windows-remote-management-glossary.md) 和作業來執行某些 api 來寫入外掛程式。 為 WinRM 服務或 Internet Information Services (IIS) 設定外掛程式之後，它們會分別載入至 WinRM 主機或 IIS 主機。 遠端要求會路由傳送至這些外掛程式進入點，以執行作業。

WinRM 外掛程式 API 參考一節包含下列 API 元素的詳細資訊：

-   [授權外掛程式進入點](authorization-plug-in-entry-points.md)
-   [授權外掛程式方法](authorization-plug-in-methods.md)
-   [作業外掛程式進入點](operations-plug-in-entry-points.md)
-   [操作外掛程式方法](operations-plug-in-methods.md)
-   [結構](winrm-plug-in-api-structures.md)

 

 




