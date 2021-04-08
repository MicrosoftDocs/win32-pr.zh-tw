---
title: 刪除應用程式目錄分割
description: 刪除表示應用程式目錄分割的交互參照物件，以刪除應用程式目錄分割。
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- 刪除應用程式目錄分割廣告
- 應用程式目錄分割廣告，刪除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681676"
---
# <a name="deleting-an-application-directory-partition"></a>刪除應用程式目錄分割

刪除表示應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件，以刪除應用程式目錄分割。 將 **交叉交叉** 物件的刪除複寫到具有應用程式目錄分割複本的網域控制站時，KCC 會刪除應用程式目錄分割的本機複本。 最後會刪除應用程式目錄分割的所有複本。

刪除 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件時，Active Directory 伺服器將會刪除建立應用程式目錄分割時所建立的 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) 物件，以及刪除應用程式目錄分割中的所有物件。 當應用程式目錄分割中的物件被刪除時，不會將它們全部刪除。

刪除應用程式目錄分割時，很難將它還原。 若要還原應用程式目錄分割，必須還原具有應用程式目錄分割複本的備份，找出代表應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件，並以系統授權方式還原 **交叉引用** 物件。

**若要刪除應用程式目錄分割及其複本，請執行下列步驟**

1.  在 [資料分割] 容器中搜尋具有與應用程式目錄分割的辨別名稱相等的 [**nCName**](/windows/desktop/ADSchema/a-ncname)屬性值的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件。
2.  刪除 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。

如需詳細資訊，請參閱 [刪除應用程式目錄分割的範例程式碼](example-code-for-deleting-an-application-directory-partition.md)。

 

 