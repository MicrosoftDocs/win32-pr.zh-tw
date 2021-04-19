---
description: 寫入器和要求者都會維護其專屬元資料檔案中的備份或還原作業所需的資訊。
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: VSS 中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972635"
---
# <a name="vss-metadata"></a>VSS 中繼資料

寫入器和要求者都會維護其專屬元資料檔案中的備份或還原作業所需的資訊。

這些檔（分別是 [*寫入器元資料檔案*](vssgloss-w.md) 和 [*備份元件檔*](vssgloss-b.md)）是用來做為寫入器和要求者通訊的基礎，以及備份和還原活動期間的協調。

中繼資料是使用專屬架構以 XML 格式表示。 中繼資料可以複製到磁片、磁帶或任何其他的大型存放裝置。 在備份作業期間，應該一律將其儲存至備份媒體，而且必須在還原作業期間從該媒體中取出。

**注意：** 格式和架構的特定詳細資料僅供系統使用。 開發人員不應該嘗試修改或直接使用中繼資料的 XML 表示。

撰寫者和要求者可透過各種查詢來提供，並設定方法來存取和修改備份元件和寫入器元資料檔案：

-   [使用寫入器元資料檔案](working-with-the-writer-metadata-document.md)
-   [使用備份元件檔](working-with-the-backup-components-document.md)
-   [VSS 中繼資料元件](vss-metadata-components.md)

 

 



