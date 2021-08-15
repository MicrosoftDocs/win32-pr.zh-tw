---
description: 下列程式描述如何安裝並存元件作為共用元件。
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: 將並存元件安裝為共用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6348354b224e281135e72697aaa155ce69f4ccd23293f671d733e2bc1cd89dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127508"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>將並存元件安裝為共用元件

下列程式描述如何安裝 [並存元件](about-side-by-side-assemblies-.md) 作為 [共用元件](/windows/desktop/Msi/shared-assemblies)。

**安裝並存元件作為共用元件**

1.  簽署並建立元件中檔案的目錄。

    檔案必須經過簽署，才能以並存元件的形式安裝檔案。 如需詳細資訊，請參閱 [建立簽署的檔案和目錄](creating-signed-files-and-catalogs.md)。

2.  您應將共用並存元件安裝為 Windows Installer 套件的元件。 這可以是用來安裝或更新應用程式的相同安裝套件。 如果共用的元件隨附為多個應用程式的一部分，您應該提供合併模組，該模組可以併入這些應用程式的安裝套件，並為元件中的檔案建立目錄。

    Windows安裝元件時需要安裝程式2.0 版或更新版本。 如需詳細資訊，請參閱[Windows Installer](../msi/windows-installer-portal.md) SDK 和[Win32 元件安裝](../msi/installation-of-win32-assemblies.md)中的章節。

 

 
