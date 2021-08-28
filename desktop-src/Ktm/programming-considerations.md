---
description: 深入瞭解：撰寫資源管理員的程式設計考慮
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: 撰寫資源管理員的程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a20d84695a5bc0f378c8b93519a35b9a1d95bcc58d718520478e519707553b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388907"
---
# <a name="programming-considerations-for-writing-resource-managers"></a>撰寫資源管理員的程式設計考慮

使用核心交易管理員 API 將交易支援新增至您的應用程式時，請考慮下列事項：

-   當您撰寫自己的 resource manager 時，您應該具備交易管理技術和通訊協定的良好、實用知識。
-   如果您未正確寫入資源管理員，您可以使用不當處理的復原作業來損毀自己的資料。 您也可以釘選交易記錄的結尾，並將交易記錄填滿檔案系統。
-   如果您的記錄大小原則未設定為防止記錄檔大小增加，則您的 resource manager 不會停止交易。 您的資源管理員必須停止更新系統，使其不會溢出檔案系統資源。
-   資源管理員應該使用 (Acl) 的存取控制清單來控制記錄檔的存取權;否則，可能會發生阻絕服務攻擊。
-   快取資料的任何 resource manager 或交易參與者都必須登記預先準備的通知。 收到預先準備通知時，您必須排清所有資料，以便任何下游資源管理員都可以在準備階段之前登記。 該交易中的任何進一步工作都不能快取。
-   當交易仍為使用中時，請勿關閉登記控制碼;這將會回復交易。

 

 



