---
title: 使用服務連接點發佈
description: Active Directory 架構會定義 serviceConnectionPoint (SCP) 物件類別，讓服務能夠輕鬆地將服務特定的資料發佈到目錄中。
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- 使用服務連接點發佈 AD
- 服務連接點廣告
- 服務連接點廣告，發佈方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671251"
---
# <a name="publishing-with-service-connection-points"></a>使用服務連接點發佈

Active Directory 架構會定義 **serviceConnectionPoint** (SCP) 物件類別，讓服務能夠輕鬆地將服務特定的資料發佈到目錄中。 服務的用戶端會使用 SCP 中的資料來尋找、連接及驗證您的服務實例。

本節提供服務連接點和程式碼範例的總覽，說明用戶端/服務應用程式如何使用 Scp。

程式碼範例會遵循下列步驟來使用 Scp 來執行服務發行。

如需執行這些步驟的詳細資訊和程式碼範例，請參閱 [建立服務連接點](creating-a-service-connection-point.md)。

**在服務安裝的目錄中建立 Scp**

1.  系結至已安裝服務實例之主機電腦的電腦物件。
2.  建立 SCP 物件做為電腦物件的子系，並指定 SCP 屬性的初始值。
3.  在 SCP 物件的安全描述項中，將存取控制專案設定 (Ace) ，讓服務在執行時間修改 SCP 屬性。
4.  在服務主機電腦上的登錄中快取 SCP 的 **objectGUID** 。

如需執行這些步驟的詳細資訊和程式碼範例，請參閱 [更新服務連接點](updating-a-service-connection-point.md)。

**在服務啟動時更新 SCP 屬性**

1.  從登錄取出 **objectGUID** ，並用它來系結至 SCP。
2.  從 SCP 取出屬性，例如 **serviceDNSName** 和 **serviceBindingInformation**。 將這些值與目前的值相比較，並視需要更新 SCP。

如需執行這些步驟的詳細資訊和程式碼範例，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。

**若要透過用戶端應用程式尋找並使用 SCP**

1.  系結至通用類別目錄，並搜尋具有符合服務產品 GUID 之 **關鍵字** 屬性的物件。 每個找到的物件都是服務的實例。 選取實例並取出 SCP 的分辨名稱。
2.  使用該辨別名稱來繫結到 SCP。
3.  從 SCP 取出各種屬性的值，例如 **serviceDNSName** 和 **serviceBindingInformation**。 使用這些值連線到服務執行個體並向其驗證。

如需有關哪些角色可以建立及更新 SCP 的詳細資訊，請參閱 [服務發行的安全性問題](security-issues-for-service-publication.md)。

如需有關如何建立 SCP 的詳細資訊，請參閱 [建立服務連接點的位置](where-to-create-a-service-connection-point.md)。

如需在 SCP 中儲存之資料類型的詳細資訊，請參閱 [服務連接點屬性](service-connection-point-properties.md)。

如需有關服務安裝程式和服務如何一起運作以維護 SCP 中目前資料的詳細資訊，請參閱 [建立和維護服務連接點](creating-and-maintaining-a-service-connection-point.md)。

 

 




