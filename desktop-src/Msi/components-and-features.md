---
description: Windows Installer 會根據元件和功能的概念來組織安裝。
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: 元件和功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cea0d384b3ad2bc3238178ae0f5811c3bad7b501068bcecd35d4c5b36d922a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144554"
---
# <a name="components-and-features"></a>元件和功能

Windows Installer 會根據元件和功能的概念來組織安裝。

功能是應用程式的總功能的一部分，使用者可能會決定個別安裝。 如需詳細資訊，請參閱[Windows Installer 功能](windows-installer-features.md)。

元件是要安裝的應用程式或產品的一部分。 安裝程式一律會從使用者的電腦安裝或移除元件，做為一致的部分。 元件通常會隱藏在使用者之外。 當使用者選取安裝的功能時，安裝程式會決定必須安裝哪些元件才能提供該功能。 如需詳細資訊，請參閱[Windows Installer 元件](windows-installer-components.md)。

安裝套件的作者必須決定如何將其應用程式分成功能和元件。 特性的選擇主要取決於應用程式從使用者的觀點來看的功能。 因為通常必須在應用程式之間共用元件，或甚至是在各產品之間共用元件，所以建議作者遵循標準方法來選取元件。 如需詳細資訊，請參閱將 [應用程式組織成元件](organizing-applications-into-components.md)。

 

 



