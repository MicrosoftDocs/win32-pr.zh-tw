---
title: 新增、刪除和取代資源
description: 本主題討論如何新增、刪除或取代資源。
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c12a1531e422efe44cbd0b3deca9f89838698
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968650"
---
# <a name="adding-deleting-and-replacing-resources"></a>新增、刪除和取代資源

應用程式必須經常新增、刪除或取代可執行檔中的資源。 您可以使用兩種方法來完成這些工作。 第一個是編輯資源定義檔、重新編譯資源，然後將重新編譯的資源新增到應用程式的可執行檔。 第二種方法是將資源資料直接複製到應用程式的可執行檔。

例如，若要將英文版的應用程式當地語系化以用於挪威，可能需要使用挪威文來取代英文對話方塊。 開發人員會使用對話方塊編輯器或在資源定義檔中撰寫範本，建立適當的對話方塊。 然後，開發人員會重新編譯資源，並將新的資源加入至應用程式的可執行檔。

但是，如果二進位格式有適當的對話方塊，開發人員可以使用下列函式，將資料直接複製到當地語系化的可執行檔。 [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)函式會建立要變更其資源之可執行檔的更新控制碼。 [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea)函式會使用此控制碼來新增、刪除或取代可執行檔中的資源。 [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)函式會關閉控制碼。

在 [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)建立可執行檔的更新控制碼之後，應用程式可以重複使用 [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) 來變更資源資料。 對 **UpdateResource** 的每個呼叫都會參與新增、刪除和取代的內部清單，但實際上不會將資料寫入至可執行檔。 [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)會在關閉更新控制碼之前立即將累積的變更寫入至可執行檔。

有時候，應用程式必須從另一個檔案複製資源。 [更新資源](using-resources.md) 會顯示從檔案取得資源資料和其大小的範例。

 

 




