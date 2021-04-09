---
description: 包含一或多個目錄的目錄是包含的目錄或目錄的父系，而每個包含的目錄都是父目錄的子系。 目錄的階層式結構稱為目錄樹狀目錄。
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: 關於目錄管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848061"
---
# <a name="about-directory-management"></a>關於目錄管理

包含一或多個目錄的目錄是包含的目錄或目錄的 *父系* ，而每個包含的目錄都是父目錄的 *子* 系。 目錄的階層式結構稱為 *目錄樹狀目錄*。

NTFS 檔案系統會將目錄和其所包含之檔案之間的邏輯連結，實作為 *目錄專案資料表*。 當檔案移至目錄時，會在表格中為移動的檔案建立一個專案，並將該檔案的名稱放在專案中。 當刪除包含在目錄中的檔案時，也會從資料表中刪除對應至已刪除檔案的名稱和專案。 目錄專案資料表中可以有一個以上的單一檔案專案。 如果在資料表中為檔案建立額外的專案，該專案就稱為該檔案的永久 *連結* 。 可以為單一檔案建立的永久連結數目沒有任何限制。

目錄也可以包含聯接和重新分析點。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                 | 描述                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [建立和刪除目錄](creating-and-deleting-directories.md)<br/> | 應用程式可透過程式設計方式建立和刪除目錄。<br/>                          |
| [目錄控制碼](obtaining-a-handle-to-a-directory.md)<br/>                 | 只要進程建立或開啟目錄物件，它就會收到物件的控制碼。<br/> |
| [重新剖析點](reparse-points.md)<br/>                                       | 描述重新分析點。<br/>                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[目錄管理參考](directory-management-reference.md)
</dt> </dl>

 

 




