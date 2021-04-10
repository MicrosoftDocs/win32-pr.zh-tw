---
description: Windows Installer 可以執行應用程式或產品的系統管理安裝，以供工作組使用。
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: 系統管理安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3958bdc81ee43cd1a36e0d464f3e77032b4c2d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026646"
---
# <a name="administrative-installation"></a>系統管理安裝

Windows Installer 可以執行應用程式或產品的系統管理安裝，以供工作組使用。 系統管理安裝會將應用程式的來源映射安裝到網路上，其類似于 CD-ROM 上的來源映射。 工作組中具有此系統管理映射存取權的使用者，可以從這個來源安裝產品。 使用者必須先從網路安裝產品，才能執行應用程式。 使用者可以選擇在安裝時從來源執行，而且安裝程式會直接從網路使用大部分產品的檔案。

系統管理員可以使用/a [命令列選項](command-line-options.md)，從命令列執行系統管理安裝。

系統 [管理員動作](admin-action.md) 是用來起始系統管理安裝的最上層動作。 執行此動作時，安裝程式會呼叫 [AdminExecuteSequence](adminexecutesequence-table.md) 和 [AdminUISequence](adminuisequence-table.md) 資料表中的動作，以執行系統管理安裝。

[**AdminProperties**](adminproperties.md)屬性是在系統管理安裝時所設定的屬性清單（以分號分隔）。 安裝程式會在應用程式的後續管理安裝期間，從系統管理映射使用這些屬性。

沒有連續存取網路的使用者，可能會從系統管理映射安裝應用程式，然後有時必須依賴媒體（如 CD-ROM 磁片）作為其備份來源。 在這些情況下，系統管理影像和媒體上的檔案名長度必須相符。 兩者都必須使用長檔名，或兩者都必須使用簡短的檔案名。 例如，只支援簡短檔案名的 CD-ROM 可以提供原始媒體來安裝系統管理映射和備份來源。

如果在系統管理安裝期間設定了 [**SHORTFILENAMES**](shortfilenames.md) 屬性，則使用者可能需要再次設定此屬性，然後將修補程式套用至系統管理映射。 使用 Windows Installer 套用修補程式時，如果系統管理映射使用簡短的檔案名，安裝程式會自動設定 **SHORTFILENAMES** 屬性。

如果系統管理員使用具有 [ [**字數統計摘要**](word-count-summary.md) ] 屬性2或3的封裝來執行系統管理安裝，系統管理映射的使用者將無法從原始媒體來源自動重新安裝。 如果系統管理映射無法使用，已從系統管理映射安裝的使用者將無法還原到原始媒體。

在系統管理映射建立期間， [*轉換*](t-gly.md) 的應用程式沒有任何有效的效果。 若要將自訂版本的產品提供給工作群組，請從系統管理映射在產品安裝期間套用轉換。

在系統管理安裝期間，安裝程式會針對產品中的所有功能建立來源映射，但 [功能資料表](feature-table.md)的 [層級] 資料行中有0的功能除外。

 

 



