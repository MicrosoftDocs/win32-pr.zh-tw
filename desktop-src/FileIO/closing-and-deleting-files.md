---
description: 若要有效率地使用作業系統資源，應用程式應該在不再需要使用 CloseHandle 函式時關閉檔案。 如果在應用程式終止時開啟檔案，系統會自動將它關閉。
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: 關閉和刪除檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c74ad36f2f099b8d2430f52cc2c40b789862c691f56df1ccebcd20e82586ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696298"
---
# <a name="closing-and-deleting-files"></a>關閉和刪除檔案

若要有效率地使用作業系統資源，應用程式應該在不再需要使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式時關閉檔案。 如果在應用程式終止時開啟檔案，系統會自動將它關閉。

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)函式可以在關閉時用來刪除檔案。 您必須先關閉檔案的所有控制碼，才能刪除檔案。 如果無法刪除檔案，則無法重複使用其名稱。 若要立即重複使用檔案名，請重新命名現有的檔案。

如果您要在遠端電腦上刪除開啟的檔案或目錄，但在遠端電腦上已開啟該檔案或目錄，但未設定「讀取共用」許可權，請不要呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 或 [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) 來開啟檔案或目錄以供先刪除。 這麼做會導致共用違規。

 

 
