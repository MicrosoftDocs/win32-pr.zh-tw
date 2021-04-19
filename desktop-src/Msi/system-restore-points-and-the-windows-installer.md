---
description: 系統還原會自動監視並記錄使用者電腦上的重要系統變更。 如需詳細資訊，請參閱系統還原。
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: 系統還原點和 Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000084"
---
# <a name="system-restore-points-and-the-windows-installer"></a>系統還原點和 Windows Installer

系統還原會自動監視並記錄使用者電腦上的重要系統變更。 如需詳細資訊，請參閱 [系統還原](../sr/system-restore-portal.md)。

系統還原點是由系統建立的，而且也會在安裝或移除軟體時 Windows Installer 建立。

在 Windows XP 中，安裝程式可能會在第一次安裝應用程式期間，以及在移除時建立檢查點。 只有在使用 [*基本 UI*](b-gly.md)執行變更時，安裝程式才會在這些情況下建立檢查點。 [使用者介面層級](user-interface-levels.md)設定為 [無] 的安裝通常是由系統或應該處理建立檢查點的應用程式所起始。 如需詳細資訊，請參閱 [系統還原](../sr/system-restore-portal.md)。

在具有許多小型應用程式的公司中，系統管理員可能會決定停用安裝程式內的檢查點，以改善效能。 如需詳細資訊，請參閱 [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) 或 [設定自訂動作的還原點](setting-a-restore-point-from-a-custom-action.md)。

從 Windows Installer 5.0 開始，可以設定 [**MSIFASTINSTALL**](msifastinstall.md) 屬性，以防止安裝產生系統還原點。

 

 
