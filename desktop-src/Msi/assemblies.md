---
description: Windows Installer 可以安裝、移除及更新由 Microsoft .NET Framework 的 common language runtime 所使用的 Win32 元件和元件。
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: 組件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981538"
---
# <a name="assemblies"></a>組件

Windows Installer 可以安裝、移除及更新由 Microsoft .NET Framework 的 common language runtime 所使用的 Win32 元件和元件。 元件是以單一安裝程式元件的 Windows Installer 來處理。 構成元件的所有檔案都必須包含在 [元件](component-table.md) 資料表中所列的單一安裝程式元件中。

在 Windows Vista 和 Windows XP 上執行的 Windows Installer 可以安裝並存元件。 並存元件可以安全地在多個應用程式之間共用元件，並可抵消元件共用的負面影響，例如 DLL 衝突。 除了會假設與所有應用程式回溯相容的單一版本元件之外，並存元件共用也可讓多個版本的 COM 或 Win32 元件在系統上同時執行。 這項增強功能可隔離應用程式是 Microsoft .NET Framework 的重要部分。 如需詳細資訊，請參閱 [隔離的應用程式和並存元件](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)。

下列各節描述如何搭配使用元件與 Windows Installer。

-   [將元件加入封裝中](adding-assemblies-to-a-package.md)
-   [安裝和移除元件](installing-and-removing-assemblies.md)
-   [更新組件](updating-assemblies.md)
-   [Common Language Runtime 元件的重新安裝模式](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Windows Installer 所寫入的元件登錄機碼](assembly-registry-keys-written-by-windows-installer-.md)

如需安裝 COM 和 COM + 1.0 應用程式的詳細資訊，請參閱 [安裝具有 Windows Installer 的 COM + 應用程式](installing-a-com--application-with-the-windows-installer.md)、將 [com 元件安裝至私用位置](installing-a-com-component-to-a-private-location.md)，以及 [將 com 元件設為私用的現有封裝](make-a-com-component-in-an-existing-package-private.md)。

 

 
