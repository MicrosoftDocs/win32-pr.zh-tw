---
description: 共用元件是可供電腦上的多個應用程式使用的元件。
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: 關於共用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5db7f10ea5ffa6e04fd5cd905262eb026b4ca4c24309ffd4c53cb10f9df00b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142621"
---
# <a name="about-shared-assemblies"></a>關於共用元件

共用元件是可供電腦上的多個應用程式使用的元件。 在 Windows Vista 和 Windows XP 上，[並存元件](about-side-by-side-assemblies-.md)可以安裝為共用的元件。 共用並存元件並不會在系統上進行全域登錄，但在 [資訊清單](manifests.md)中指定對元件之相依性的應用程式可全域使用。 並行元件的多個版本可由同時執行的不同應用程式共用。 如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](about-isolated-applications-and-side-by-side-assemblies.md)。 例如，隨附于 Windows XP 的[支援 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)，通常是由多個應用程式用來作為共用的元件。

共用並存元件會安裝在 WinSxS 資料夾中。 元件發行者、應用程式和系統管理員 [可以在部署](configuration.md)完成之後，變更並存元件相依性的版本。 共用並存元件可以由作業系統更新或安裝或更新應用程式的 Windows Installer 套件來安裝。 如需詳細資訊，請參閱 [Win32 元件的安裝](../msi/installation-of-win32-assemblies.md)。

在 Windows XP 之前，共用的元件是全域註冊，並安裝在 Windows 系統資料夾中。 在此情況下，元件的最新安裝版本可供任何系結至該元件的應用程式使用。 並存元件也可以安裝為私用元件，以用於應用程式的專屬用途。 如需詳細資訊，請參閱 [私用組件](/windows/desktop/Msi/private-assemblies)。

 

 
