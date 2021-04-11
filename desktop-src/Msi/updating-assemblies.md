---
description: 本主題中的資訊會識別使用 Windows Installer 修補程式來更新元件的建議指導方針。
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: 更新組件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b185a9943ba20c81a1fa3431dd590eb05648c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027569"
---
# <a name="updating-assemblies"></a>更新組件

本主題中的資訊會識別使用 Windows Installer 修補程式來更新元件的建議指導方針。

元件更新的作者可以使用下列指導方針，其適用于所有類型的元件：

-   更新元件的建議方法是在 [MsiAssemblyName 資料表](msiassemblyname-table.md)中變更元件的強式名稱。 新元件版本可由新元件或提供舊版本的相同元件提供。
-   如果新的元件版本是由相同的元件所提供，請勿將元件類型從 .NET Framework 元件變更為 Win32 元件，反之亦然。
-   如果系統上的所有應用程式都必須使用更新的元件，您應該部署原則元件。 原則元件可以重新導向系統上的應用程式，以使用新的元件版本。 您應藉由建立新的元件來提供原則元件。
-   需要 Windows Installer 3.0 或更新版本，才能卸載元件更新。 如需詳細資訊，請參閱 [移除修補程式](removing-patches.md)。
-   較新版本的元件應該包含先前發行之元件中的相同或更高版本的檔案。
-   Windows Installer 3.0 可以透過完整的檔案取代或較小的差異更新來服務 .NET Framework 和 Win32 元件。 如需詳細資訊，請參閱 [減少修補程式大小](reducing-patch-size.md)。
-   如果您的更新變更元件的強式名稱，則如果 patch 封裝沒有[MsiPatchSequence](msipatchsequence-table.md)資料表，則需要[MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md)資料表和[MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md)資料表。 如果 patch 封裝在 MsiPatchSequence 資料表中有修補程式的排序資訊，則不需要 MsiPatchOldAssemblyFile 資料表和 MsiPatchOldAssemblyName 資料表。
-   發行新的修補程式之前，請先將修補程式套用至所有先前發行的修補程式，以測試修補程式。

## <a name="updating-win32-assemblies"></a>更新 Win32 元件

當您更新 Win32 元件時，請使用下列指導方針：

-   變更 [MsiAssemblyName 資料表](msiassemblyname-table.md)中所指定之新元件的強式名稱。
-   如果您希望應用程式一律使用新版本的元件，而不會影響系統上其他應用程式所使用的元件版本，請使用相同的元件來包含您用於舊元件版本的新元件版本。 在 [元件](component-table.md) 資料表中保留相同的元件。 當您的應用程式經過修補之後，它只會保存新版元件的參考。 舊版元件可以保留在全域組件快取中的新版本。 這不會影響使用舊版元件的系統上的其他應用程式。 當相同元件同時用於新舊版本的元件時，您的更新可以是較小的 delta 修補程式。
-   如果新版本的元件與您想要安裝應用程式的所有系統不相容，您可以將新舊版本的元件安裝為並存元件。 若要並存安裝這兩個元件版本，請建立新的元件以包含新的元件版本。 新元件的 [元件](component-table.md) 資料表中的元件元件應該與舊版元件的元件元件不同。 在您的應用程式修補之後，它會同時保有兩個元件版本的參考。 然後，應用程式可以透過資訊清單導向至相容的元件版本。 當新舊版本的元件使用不同的元件時，您的更新會使用完整的檔案取代。

## <a name="updating-net-framework-assemblies"></a>更新 .NET Framework 元件

當您更新 .NET Framework 元件時，請使用下列指導方針。

-   變更 [MsiAssemblyName 資料表](msiassemblyname-table.md)中所指定之新元件的強式名稱。
-   如果您想要讓應用程式一律使用新版的元件，而不會影響系統上其他應用程式所使用的元件版本，請變更 [MsiAssemblyName 資料表](msiassemblyname-table.md)中所指定之新元件的強式名稱，並使用相同的元件來包含您用於舊元件版本的新元件版本。 在 [元件](component-table.md) 資料表中保留相同的元件。 當您的應用程式經過修補之後，它只會保存新版元件的參考。 舊版元件可以保留在全域快取中的新版本。 這不會影響使用舊版元件的系統上的其他應用程式。 當相同元件同時用於新舊版本的元件時，您的更新可以是較小的 delta 修補程式。
-   如果新版本的元件與您想要安裝應用程式的所有系統不相容，您可以將新舊版本的元件安裝為並存元件。 若要並存安裝這兩個元件版本，請變更 [MsiAssemblyName 資料表](msiassemblyname-table.md)中所指定之新元件的強式名稱，然後建立新的元件以包含新的元件版本。 新元件的 [元件](component-table.md) 資料表中的元件元件應該與舊版元件的元件元件不同。 在您的應用程式修補之後，它會同時保有兩個元件版本的參考。 然後，應用程式可以透過資訊清單導向至相容的元件版本。 當新舊版本的元件使用不同的元件時，您的更新會使用完整的檔案取代。
-   就地更新會覆寫全域組件快取中 .NET Framework 元件的複本。 這種類型的元件更新不會變更元件的強式名稱。 只有 [MsiAssemblyName 資料表](msiassemblyname-table.md) 的 FileVersion 欄位中的值會變更。 .NET Framework 元件的就地更新需要 .NET Framework 1.1 SP1 或更新版本。
    > [!Note]  
    > 就地更新類型會覆寫全域快取中的元件複本，而且如果新版本的元件不完全相容，則可能會中斷其他應用程式。 更新元件的建議方法是在 [MsiAssemblyName 資料表](msiassemblyname-table.md)中變更元件的強式名稱。

     

 

 



