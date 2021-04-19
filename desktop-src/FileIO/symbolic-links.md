---
description: 符號連結是指向另一個檔案系統物件的檔案系統物件。 所指向的物件稱為「目標」。
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: 符號連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994465"
---
# <a name="symbolic-links"></a>符號連結

符號連結是指向另一個檔案系統物件的檔案系統物件。 所指向的物件稱為「目標」。

符號連結對使用者而言是透明的;這些連結會顯示為一般檔案或目錄，並可由使用者或應用程式以完全相同的方式處理。

符號連結是設計來協助與 UNIX 作業系統進行遷移和應用程式相容性。 Microsoft 已實作為其符號連結的運作方式，就像 UNIX 連結一樣。

如需詳細資訊，請參閱下列主題。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                             | 描述                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [檔案系統函數的符號連結效果](symbolic-link-effects-on-file-systems-functions.md)<br/> | 符號連結如何影響使用路徑名稱來指定一個或多個檔案的標準檔案函數。<br/>                                        |
| [程式設計考量](symbolic-link-programming-considerations.md)<br/>                             | 使用符號連結的程式設計考慮。<br/>                                                                                |
| [建立符號連結](creating-symbolic-links.md)<br/>                                                 | 使用 [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) 函數建立使用絕對或相對路徑的符號連結。<br/> |



 

## <a name="supported-operating-systems"></a>支援的作業系統

從 Windows Vista 開始，NTFS 提供符號連結。

 

 




