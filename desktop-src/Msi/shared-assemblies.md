---
description: Win32 元件可以安裝為共用的元件，並且可供電腦上的多個應用程式使用。 共用的元件應該由用來安裝或更新應用程式的 Windows Installer 套件進行安裝。
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: 共用組件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693848"
---
# <a name="shared-assemblies"></a>共用組件

Win32 元件可以安裝為共用的元件，並且可供電腦上的多個應用程式使用。 共用的元件應該由用來安裝或更新應用程式的 Windows Installer 套件進行安裝。

共用的元件會以 [並存元件](side-by-side-assemblies.md)的形式安裝。 Windows Installer 會將共用的並存元件安裝到 Winsxs 資料夾中。 元件不會在系統上全域註冊，但是在資訊清單檔中指定元件相依性的任何應用程式都可以全域使用這些元件。 如需詳細資訊，請參閱 [隔離的應用程式和並存元件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)。

在 Windows XP 之前的作業系統上，共用的元件通常會安裝在 Windows system 資料夾中，並在全域註冊。 已安裝的最新版本可供任何系結至該版本的應用程式使用。

如需如何撰寫 Windows Installer 套件以安裝共用元件的詳細資訊，請參閱下列內容：

-   [在 Windows XP 上安裝適用于並存共用的 Win32 元件](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [在 Windows XP 上安裝 Win32 元件以私用應用程式](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
