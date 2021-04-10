---
title: 命名內容和目錄分割
description: 由 Active Directory Domain Services 所控制之網域樹系中的每個網域控制站都包含目錄分割。
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- 命名內容和目錄分割的 AD
- 命名內容 AD，關於
- 目錄分割廣告，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39934f0236e927bff281230c41a303f5e6d2bb0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933054"
---
# <a name="naming-contexts-and-directory-partitions"></a>命名內容和目錄分割

由 Active Directory Domain Services 所控制之網域樹系中的每個網域控制站都包含 [*目錄*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85))分割。 目錄分割也稱為 [*命名內容*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85))。 目錄分割是整體目錄的連續部分，其具有獨立的複寫範圍和排程資料。 根據預設，企業的 Active Directory 網域服務包含下列磁碟分割：

-   [*架構分割*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85))區：架構分割區包含 **classSchema** 和 **attributeSchema** 物件，可定義樹系中可以存在的物件類型。 樹系中的每個網域控制站都有相同架構資料分割的複本。
-   設定 [*磁碟分割*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85))：設定磁碟分割包含複寫拓撲，以及必須在整個樹系中複寫的其他設定資料。 樹系中的每個網域控制站都有相同設定分割區的複本。
-   [*網域分割*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85))區：網域分割區包含與本機網域相關聯的目錄物件，例如使用者和電腦。 網域可以有多個網域控制站，而一個樹系可以有多個網域。 每個網域控制站都會針對其本機網域儲存網域分割區的完整複本，但不會儲存其他網域的網域分割區複本。

Windows Server 2003 引進 *應用程式目錄分割*，可讓您控制複寫的範圍，並允許以更適合動態資料的方式放置複本。 如需應用程式目錄分割的詳細資訊，請參閱 [關於應用程式目錄](about-application-directory-partitions.md)分割。

如需 Active Directory Domain Services 如何在目錄分割的各種複本之間保持一致性的詳細資訊，請參閱複寫 [和資料完整性](replication-and-data-integrity.md)。

 

 