---
description: 下列指導方針討論如何撰寫您自己的 COM 或 Win32 並存元件。
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: 建立並存元件的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19054f0c48f74a373f0ce502cb6b52374db5ded00fcde3c284fad2609ba21e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885248"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>建立並存元件的指導方針

下列指導方針討論如何撰寫您自己的 COM 或 Win32 並存元件。 如果所需的功能是由其中一個 [支援的 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)所提供，您可能不需要建立自己的並存元件。 在此情況下，請使用 Microsoft 提供的元件，並遵循在 [使用隔離的應用程式和並存元件](using-isolated-applications-and-side-by-side-assemblies.md)中使用並存元件的程式。

首先，請考慮您的元件是否為並存元件提供合適的候選。 如需詳細資訊，請參閱是否 [應將共用元件提供為並存元件？](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md)

若要建立並存元件，請遵循下列指導方針：

-   決定要包含在元件中的資源。 請記住，元件是由一或多個永遠提供給應用程式和客戶的檔案所組成。 元件是用來命名、系結、版本控制、部署和 [預設](default-configuration.md)設定的基礎單位。 一般而言，如果不確定兩個資源是否屬於相同的元件，建議您將它們撰寫成可移至不同的元件。 通常，並存元件是由單一 DLL 組成。
-   建立元件的程式集 [清單](manifests.md) 。 資訊清單應該描述元件中的 COM 物件或類型程式庫。 如需有關要在組件資訊清單中編寫哪些內容的詳細資訊，請參閱 [程式集](assembly-manifests.md)清單。
-   當您在系統上執行一個以上的元件版本時，請評估物件的使用方式。 判斷元件的不同版本是否需要個別的資料結構，例如記憶體對應檔、具名管道、註冊 Windows 訊息和類別、共用記憶體、信號、mutex 和硬體驅動程式。 跨元件版本使用的任何資料結構都必須是回溯相容的版本。 決定可在不同版本之間使用的資料結構，以及哪些資料結構必須是私用的版本。 判斷共用資料結構是否需要個別的同步處理物件，例如信號和 mutex。
-   藉由遵循 [針對並存元件撰寫 DLL](authoring-a-dll-for-a-side-by-side-assembly.md)的指導方針，撰寫您的 DLL 以做為並存元件。
-   撰寫一組標頭檔和 helper 函式，以提供簡單的方式來將包含元件狀態的登錄機碼設定為版本。 元件通常會將其狀態設定儲存在登錄機碼中。 登錄設定必須以個別版本撰寫，以隔離可同時執行的多個元件版本。 設計並存元件和 DLL，在並存共用案例期間，正確地儲存和處理元件的狀態。 遵循[針對並存元件撰寫狀態儲存體](authoring-state-storage-for-side-by-side-assemblies.md)的指導方針。
-   使用 [私用元件](/windows/desktop/Msi/private-assemblies) 的應用程式開發人員應該保護應用程式目錄。 如果使用[Windows Installer](../msi/windows-installer-portal.md)安裝應用程式，則可以使用 LockPermissions 資料表來保護應用程式目錄。 一般而言，系統會提供私用元件的讀取、寫入和執行存取權;所有其他進程僅提供執行和讀取存取權。
-   使用並存共用的案例來測試元件，以確保它是有效的並存元件。 成功安裝元件並不足以保證它會如預期般運作。
-   採用方法來為您的元件編號更新。 每個元件都與四部分版本號碼相關聯。 從左至右，主要、次要、組建和修訂部分會以句號分隔。 針對與舊版不相容的版本，變更元件的主要或次要數目。 只變更元件的回溯相容性變更的組建和修訂部分。 例如，開發人員可能會採用所有1.0.0 的編號方法。 \* 版本號碼指的是元件1.0.0.0 版的更新版本。

 

 
