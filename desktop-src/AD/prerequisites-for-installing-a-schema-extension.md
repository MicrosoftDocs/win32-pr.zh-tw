---
title: 安裝架構延伸模組的必要條件
description: 若要修改架構，請確定您擁有下列許可權，並注意下列資訊：您必須擁有足夠的許可權才能修改架構。
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314373"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a>安裝架構延伸模組的必要條件

若要修改架構，請確定您擁有下列許可權，並注意下列資訊：

-   您必須有足夠的許可權才能修改架構。 架構包含整個企業 Active Directory Domain Services 的所有資料定義。 若要更新架構，使用者必須是架構系統管理員群組的成員，或已被委派更新架構的許可權。
-   您只能在架構主機上進行架構變更。 如需詳細資訊，請參閱偵測 [架構主機](detecting-the-schema-master.md)。
-   架構主機必須是可寫入的;也就是說，必須移除登錄中的安全聯鎖。 如需詳細資訊，請參閱 [在架構主機上啟用架構變更](enabling-schema-changes-at-the-schema-master.md)。
-   如需如何檢查架構主機是否可以修改的詳細資訊，以及如何變更其設定，請參閱說明及支援知識庫中的「XADM：無法更新架構擁有者的架構」 [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) 。

 

 




