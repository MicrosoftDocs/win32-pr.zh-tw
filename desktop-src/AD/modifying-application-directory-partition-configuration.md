---
title: 修改應用程式目錄分割設定
description: 您可以藉由變更代表應用程式目錄分割的交互參照物件的某些屬性來修改應用程式目錄分割。
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- 修改應用程式目錄分割設定 AD
- 應用程式目錄分割 AD，修改設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c976c297e8491dbb87a32cf2241446ca0403e7f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842067"
---
# <a name="modifying-application-directory-partition-configuration"></a>修改應用程式目錄分割設定

您可以藉由變更代表應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件的某些屬性來修改應用程式目錄分割。 若要找出表示特定應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件，請在 [分割區] 容器中搜尋具有與應用程式目錄分割之辨別名稱相同的 [**nCName**](/windows/desktop/ADSchema/a-ncname)屬性值的 **交叉引用** 物件。 然後可以使用 **交叉引用** 物件的分辨名稱來系結至 **交叉引用** 物件。

下表列出可修改的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件的屬性。

| 屬性                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**複寫-通知-第一個-DSA-延遲**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | 指定在第一個複寫夥伴收到通知之前，原始物件變更之後的延遲（以秒為單位）。 如需詳細資訊，請參閱 [應用程式目錄分割](application-directory-partition-replication.md)複寫。                                                                                                   |
| [**複寫-通知-後續-DSA-延遲**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | 指定後續通知與複寫夥伴之間的第二個、第三個通知之間的延遲（以秒為單位）。 如需詳細資訊，請參閱 [應用程式目錄分割](application-directory-partition-replication.md)複寫。                                                                                                 |
| [**SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | 識別安全性子系統用來解讀該應用程式目錄分割中物件之 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) 屬性的本機網域參考的網域。 如需詳細資訊，請參閱 [應用程式目錄分割安全性](application-directory-partition-security.md)。 |
| [**高階 NC-複本-位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | 針對裝載應用程式目錄分割複本的每個網域控制站，包含 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) 物件的分辨名稱。 如需詳細資訊，請參閱 [新增或刪除應用程式目錄分割複本](adding-or-deleting-an-application-directory-partition-replica.md)。            |



 

 

 