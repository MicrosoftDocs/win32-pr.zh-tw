---
title: SIS 連結和重新分析點
description: SIS 是 NTFS 篩選器驅動程式，可將重複的檔案取代為複製時寫入連結 (稱為 SIS 連結) 指向單一備份檔，以減少這些檔案的磁片和快取額外負荷。
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- 重新分析點備份
- 單一實例存放區 (SIS) 備份，SIS 連結
- 儲存 (SIS) 備份、重新分析點的單一實例存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f89901df6ce1fea1635d4250f2884ec9baf68fb1552766564909486c8ed00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588858"
---
# <a name="sis-links-and-reparse-points"></a>SIS 連結和重新分析點

SIS 是 NTFS 篩選器驅動程式，可將重複的檔案取代為複製時寫入連結 (稱為 SIS 連結) 指向單一備份檔，以減少這些檔案的磁片和快取額外負荷。 此備份檔案包含在 [通用存放區](the-sis-common-store-and-common-store-files.md)中。 SIS 架構的執行會利用包含 SIS 連結相關資訊的重新 [分析點](/windows/desktop/FileIO/reparse-points) 。

SIS 連結會實作為稀疏檔案，通常會有大部分未配置的檔案範圍，以及重新分析點。 重新分析點的結構和內容對備份和還原應用程式而言是不透明的;不過，您的應用程式會將這些重新分析點內的資料，以及處理它們中資訊的 SIS API 函式，傳送和取出。 重新分析點中的資訊是指包含實際檔案資料的單一備份檔案。 這個備份檔稱為 [通用存放區](the-sis-common-store-and-common-store-files.md)檔案，而且存在於一般存放區中。

還原 SIS 連結時，您的還原應用程式應該執行下列步驟：

1.  判斷 SIS 連結所指向的一般存放區檔案。
2.  如果檔案不存在於一般存放區中，請將該檔案連同 SIS 連結一起還原。
3.  如果 SIS 連結指向存在於磁片上的通用存放區檔案，則只還原 SIS 連結。 回想一下，一般存放區檔案中的資料永遠不會變更，因此，如果指定的一般存放區檔案在還原時仍在磁片上，它會與備份時的內容相同，因此不需要覆寫它。

SIS 輔助備份所需的唯一額外負荷，是您的備份應用程式必須備份 SIS 連結和與備份檔案相關聯的資料。 所有 SIS 備份和還原作業都是特定磁片區的本機。

 

 