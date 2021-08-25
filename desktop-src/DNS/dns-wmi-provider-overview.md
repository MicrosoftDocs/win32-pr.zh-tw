---
title: DNS WMI 提供者總覽
description: 提供者是 Windows Management Instrumentation (WMI) 的架構元素。
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- 網域名稱系統、WMI 提供者、架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44103edba64a1f572beef9cff9b8aeb31f02344f172f42b2a7378a6fbf3677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913158"
---
# <a name="dns-wmi-provider-overview"></a>DNS WMI 提供者總覽

提供者是 *Windows Management Instrumentation (WMI)* 的架構元素。 WMI 會定義用來描述、存取和檢測物件的統一架構。 此架構的一部分是用來在特定物件上執行遠端系統管理工作之 WMI 類別的大型資料庫。

WMI 提供者可作為 WMI 和一或多個受管理物件之間的媒介。 當 WMI 收到來自管理應用程式的要求，以找出 CIM 存放庫中無法使用的資料，或是 WMI 不支援的事件通知時，它會將要求轉送到提供者。 提供者對特定網域的特定受管理物件提供資料與事件通知。 提供者會擴充類別的 WMI 架構，以允許 WMI 使用新的物件類型。 DNS WMI 提供者會定義用來查詢和設定 DNS 伺服器的類別，以及其相關聯的 DNS 區域和 DNS 記錄。

DNS WMI 提供者會向用戶端公開一些 DNS 物件，包括 DNS 伺服器、DNS 網域和 DNS RR 物件。 透過這些物件，用戶端就能夠執行 DNS 管理活動。

使用 DNS WMI 提供者時，您可以建立自己的工具來執行大部分的 DNS 伺服器管理工作。 例如，您可以建立、刪除和查看區域和記錄;重設伺服器和區域屬性;並執行例行的管理作業，例如更新區域、重載區域、重新整理區域、將區域寫回檔案或 Active Directory、暫停和繼續區域、清除快取、停止和啟動 DNS 服務，以及查看統計資料。

DNS WMI 提供者有一組在其他提供者中找不到的獨特行為。 如需類別的詳細資料，請參閱 [DNS WMI 提供者參考](dns-wmi-provider-reference.md) 。

 

 




