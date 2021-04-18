---
description: Win32 元件可以安裝為私用元件，並且可供一個應用程式使用。 私用元件應該由用來安裝或更新應用程式的 Windows Installer 套件進行安裝。
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: 私用組件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193100"
---
# <a name="private-assemblies"></a>私用組件

Win32 元件可以安裝為私用元件，並且可供一個應用程式使用。 私用元件應該由用來安裝或更新應用程式的 Windows Installer 套件進行安裝。

在 Windows XP 上，私用元件是以 [並存元件](side-by-side-assemblies.md)的形式安裝。 Windows Installer 會在應用程式私用的資料夾中安裝私用並存元件。 通常是包含應用程式可執行檔的資料夾。 私用元件上的應用程式相依性是在應用程式資訊清單檔中指定的。 如需詳細資訊，請參閱 [隔離的應用程式和並存元件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)。

在 Windows XP 之前的作業系統上，私用元件和本機檔案的複本會安裝到私人資料夾中，以供應用程式獨佔使用。 元件的版本也會在系統上全域註冊，而且可供任何系結至該元件的應用程式使用。 元件的全域版本可能是隨應用程式安裝的版本，或是較早的版本。 全域版本是由 [獨立元件](isolated-components.md)所使用的相同規則所決定。

請注意，Windows Installer 無法將私用元件安裝在路徑包含超過234個字元的位置，包括結束的 null 字元。

 

 
