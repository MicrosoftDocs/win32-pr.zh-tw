---
description: 建立您自己的並存元件時，請遵循建立並存元件的指導方針，並根據撰寫並存元件 DLL 的指導方針，編寫要包含在元件中的任何 DLL。
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: 撰寫並存元件的狀態儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dd3b3dc62726c45a03fd388864faa7f359112687f0c03fb133276eef2280ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885518"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>撰寫並存元件的狀態儲存體

建立您自己的並存元件時，請遵循 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md) ，並根據 [撰寫並存元件 dll](authoring-a-dll-for-a-side-by-side-assembly.md)的指導方針，編寫要包含在元件中的任何 DLL。

遵循下列的狀態儲存指導方針：

-   將狀態儲存體設計為向前及向後相容。 預期版本會以任何順序使用：例如，v1、v3 和 v2。
-   初始化和設定元件程式碼中元件的預設設定。 請勿將預設設定儲存在登錄中。
-   登錄設定必須以個別版本撰寫，以隔離可同時執行的多個元件版本。 設計並存元件，以便在並存共用案例期間，正確地儲存和處理元件的狀態。
-   元件通常會將狀態資訊儲存在登錄機碼中。 撰寫一組標頭檔和 helper 函式，以提供簡單的方式來將包含元件狀態的登錄機碼設定為版本。
-   儲存在登錄中的任何元件狀態資訊都必須與元件的其他版本隔離。 儲存在登錄中的狀態設定必須儲存在登錄的個別版本區段中。 登錄的 HKLM 和 HKCU 部分都需要這項功能。 例如，在下列登錄機碼下儲存元件版本 XXXX 的 HKCU 狀態設定：

    **HKCU** \\**MyCompany** \\**MyComponent** \\**VersionXXXX**

-   共用元件儲存在登錄中的任何狀態資訊都必須儲存在登錄的個別版本區段中。 例如，稱為 EnableSuperCoolFeature 的狀態設定可能會有 **TRUE** 或 **FALSE** 的值。 儲存 [*共用並存元件*](s-sbscs-gly.md) 的值，如下所示：

    **HKEY \_CurrentUser** \\ **Software** \\ **MyCompany** \\ **MyComponent** \\ **version 01.01** \\ **EnableSuperCoolFeature = TRUE**

-   私用元件儲存在登錄中的任何狀態資訊都必須儲存在登錄的個別應用程式區段中。 這會將元件的狀態設定與應用程式隔離。 您可以使用 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) 函數來設定虛擬根目錄。 例如，如果元件版本 XXYY 是 "SomeApplication" 的私用元件，則對 **GetModuleFileName** 的呼叫會傳回 "SomeApplication"，且元件的任何私用狀態設定都應該使用下列機碼來寫入：

    **HKCU** \\**MyCompany** \\**MyComponent** \\**VersionXXYY** \\**SomeApplication**

-   讓儲存在登錄中的共用狀態設定，私用至執行的元件內容。 您可以使用 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) 函數來設定虛擬根目錄。 這應針對 HKLM 和 HKCU 分支進行。
-   在理想的情況下，您應該採用持續性模型，讓應用程式維持狀態，而且不會改變登錄。 應用程式應該不需要直接接觸元件的登錄專案。 相反地，元件應該提供可儲存或還原並存相容之設定的 API 函數。
-   元件可能會將狀態設定儲存在登錄外的存放區，讓元件能夠與全域狀態互動。 並存元件可能會使用下列並存相容存放區：
    -   受保護的存放區 (*pstore*) 
    -   WinInet 快取
    -   Microsoft SQL Server

 

 
