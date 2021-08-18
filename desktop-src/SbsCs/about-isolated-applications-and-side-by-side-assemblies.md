---
description: 隔離應用程式和並存元件提供了一個解決 DLL 版本控制衝突的解決方案。 它們可讓應用程式安全地共用元件。 如需詳細資訊，請參閱共用的元件。
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: 關於隔離應用程式和並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ab72689173d4e8942d10dfc62259091574634227c3f4d252b0d87853ec9be7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142661"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>關於隔離應用程式和並存元件

[隔離應用程式](isolated-applications.md) 和 [並存元件](about-side-by-side-assemblies-.md) 提供了一個解決 [*DLL 版本控制衝突*](d-sbscs-gly.md)的解決方案。 它們可讓應用程式安全地共用元件。 如需詳細資訊，請參閱 [共用的元件](/windows/desktop/Msi/shared-assemblies)。

元件是命名、系結、版本控制、部署或設定程式設計程式碼區塊的基礎單位。 具有一般功能的應用程式可能會執行稱為模組或程式碼元件的程式設計程式碼共用區塊。 這些程式碼元件可能放在 Dll 或 COM 元件中。 元件安全共用的基礎結構稱為「並存元件共用」。

[並存元件](about-side-by-side-assemblies-.md) 是 [資訊清單](manifests.md) 和撰寫所描述的程式碼元件，讓多個版本可以同時執行，而不會彼此衝突。 當開發人員撰寫資訊清單和撰寫應用程式以使用 [並存元件共用](side-by-side-assembly-sharing.md)時，可以在系統上執行多個元件版本，而每個應用程式都可以指定應該使用的元件版本。

一般 [*並存元件*](s-sbscs-gly.md) 是具有單一資訊清單的單一 DLL。 並存元件會在資訊清單中儲存系結和 COM 啟用的相關資訊，傳統儲存在登錄中。 在某些情況下，資訊清單中指定的元件版本可以依元件發行者、應用程式開發人員或系統管理員變更（以全域或每個應用程式為基礎）。 如需詳細資訊，請參閱 [預設](default-configuration.md)設定、 [發行者](publisher-configuration.md)設定及 [每個應用程式](per-application-configuration.md)設定。

開發人員可以在其應用程式中使用由 Microsoft 或其他並存元件發行者所提供的並存元件。 例如，開發人員可以藉由設計其應用程式來使用包含 Comctl32.dll 6.0 的並存元件，來取得更新的通用控制項（例如主題）的功能。 如需 Windows XP 隨附的並存元件和資訊清單清單，請參閱[支援的 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)。 開發人員也可以建立自己的並存元件。 如需詳細資訊，請參閱 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md)。

 

 
