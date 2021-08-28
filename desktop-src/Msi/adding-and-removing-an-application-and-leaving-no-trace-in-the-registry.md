---
description: 如果必須註冊應用程式，請依照在安裝或移除元件時新增和移除登錄機碼一節中所述的方式來撰寫安裝套件。
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: 新增和移除應用程式，而不在登錄中保留任何追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6d3884a91efefac9cab1409a36e1843941469aae9822154be5534313b05c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105458"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a>新增和移除應用程式，而不在登錄中保留任何追蹤

如果必須註冊應用程式，請依照在 [安裝或移除元件時新增和移除登錄機碼](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)一節中所述的方式來撰寫安裝套件。 註冊是由安裝程式用於公告，以及由主控台中的 [新增或移除程式] 功能使用。 如果未註冊應用程式，則無法通告，也不會列在主控台的 [新增或移除程式] 功能中。

您可以從[InstallExecuteSequence 資料表](installexecutesequence-table.md)和[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中移除[RegisterProduct 動作](registerproduct-action.md)、 [RegisterUser 動作](registeruser-action.md)、 [PublishProduct 動作](publishproduct-action.md)和[PublishFeatures 動作](publishfeatures-action.md)，以省略註冊應用程式。 所有這些動作都必須移除，否則應用程式的某些追蹤可能會保留在登錄中。 移除所有這些動作可防止應用程式列在主控台的 [新增或移除程式] 功能中，並防止應用程式的公告。 移除所有這些動作也會導致應用程式無法向 Windows Installer 設定資料進行註冊。 這表示您無法使用 Windows Installer[命令列選項](command-line-options.md)或 Windows Installer 應用程式開發介面 (API) ，來移除、修復或重新安裝應用程式。

若要從主控台中的 [新增或移除程式] 功能隱藏應用程式，且仍然能夠使用 Windows Installer 來管理應用程式，請將註冊動作保留在順序資料表中，並將 [屬性工作表](property-table.md)中的 [**ARPSYSTEMCOMPONENT 屬性**](arpsystemcomponent.md)設定為 1 (一個) 。 應用程式不會出現在 [新增或移除程式] 功能中，但您可以使用 Windows Installer 安裝隨選安裝、卸載、修復和重新安裝應用程式。

 

 



