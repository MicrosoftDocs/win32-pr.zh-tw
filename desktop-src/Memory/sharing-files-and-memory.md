---
description: 檔案對應可以用來在兩個或多個進程之間共用檔案或記憶體。 若要共用檔案或記憶體，所有進程都必須使用相同檔案對應物件的名稱或控制碼。
ms.assetid: 942cb50d-df07-444f-bba5-58194556ae66
title: 共用檔案和記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d402eba3f87f1f799593ae0d6b23fba06124a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690540"
---
# <a name="sharing-files-and-memory"></a>共用檔案和記憶體

檔案對應可以用來在兩個或多個進程之間共用檔案或記憶體。 若要共用檔案或記憶體，所有進程都必須使用相同檔案對應物件的名稱或控制碼。

為了共用檔案，第一個進程會使用 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數來建立或開啟檔案。 接著，它會使用 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 函式來建立檔案對應物件，並指定檔案控制代碼和檔案對應物件的名稱。 事件、信號、mutex、可等候計時器、作業和檔案對應物件的名稱會共用相同的命名空間。 因此，如果 **CreateFileMapping** 和 [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) 函式指定的名稱是由其他類型的物件所使用，則這些函數會失敗。

若要共用與檔案沒有關聯的記憶體，處理常式必須使用 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 函式，並將不正確 \_ 控制碼 \_ 值指定為 *hFile* 參數，而不是現有的檔案控制代碼。 對應的檔案對應物件會存取系統分頁檔案所支援的記憶體。 當您 \_ \_ 在呼叫 **CreateFileMapping** 時指定了不正確控制碼值 hFile 時，您必須指定大於零的大小。

若要讓其他進程取得第一個進程所建立之檔案對應物件的控制碼，最簡單的方式是使用 [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) 函式，並指定物件的名稱。 這稱為「 *共用記憶體*」。 如果檔案對應物件沒有名稱，則處理常式必須透過繼承或重複來取得它的控制碼。 如需繼承和重複的詳細資訊，請參閱 [繼承](../procthread/inheritance.md)。

共用檔案或記憶體的進程必須使用 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 或 [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) 函數來建立檔案。 它們必須使用信號、mutex、事件或其他其他互斥技巧來協調其存取。 如需詳細資訊，請參閱 [同步](../sync/synchronization.md)處理。

除非使用 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函式，否則共用檔案對應物件將不會被終結，直到使用它的所有進程關閉其控制碼為止。

如需檔案對應物件安全性的詳細資訊，請參閱檔案 [對應安全性和存取權限](file-mapping-security-and-access-rights.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立命名的共用記憶體](creating-named-shared-memory.md)
</dt> </dl>

 

 
