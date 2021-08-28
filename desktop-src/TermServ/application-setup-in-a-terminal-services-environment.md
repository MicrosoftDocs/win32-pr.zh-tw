---
title: 應用程式設定
description: 針對單一使用者安裝應用程式，可能會在多使用者遠端桌面服務環境中產生問題。
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743eff150edf5e9d213759ccef8c786bab98754b8e4dc2b968929ba3ad2d6709
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099588"
---
# <a name="application-setup"></a>應用程式設定

許多現有應用程式的自動化安裝程式會假設應用程式是針對單一使用者進行安裝。 在多使用者遠端桌面服務環境中，這項假設可能會產生下列問題：

-   如果安裝程式只為一位使用者更新登錄和桌面環境，則其他使用者必須重新安裝整個封裝，否則系統管理員必須手動將資訊從登錄和使用者的桌面複製到其他使用者。
-   透過某些安裝程式，您可以藉由排除功能，在安裝時自訂應用程式。 如果初始安裝程式排除應用程式的一部分，則其他使用者必須重新安裝應用程式，才能取得排除的功能。

若要避免這些問題，安裝程式在遠端桌面工作階段主機 (RD 工作階段主機) server 上安裝應用程式時，應該使用下列指導方針：

-   將應用程式安裝在所有使用者通用的預設使用者環境中。 在安裝應用程式之前，請執行 **change user/install** console 命令，並在安裝完成之後，執行 **change user/execute** console 命令。 使用遠端桌面服務相容性腳本進行安裝。
-   透過使用者設定檔的使用，支援使用者特定的自訂。 若要這樣做，請建立系統 [管理範本檔案格式](/previous-versions/windows/desktop/Policy/administrative-template-file-format) ，讓系統管理員可以設定登錄來指出每個使用者可用的功能。 然後，在執行時間，應用程式可以根據目前使用者的登錄設定中的設定來啟用或停用功能。 應用程式可以將每個使用者設定儲存在 **HKEY CURRENT user** 登錄區中，並讓每個使用者根據其喜好設定來設定應用程式。

 

 