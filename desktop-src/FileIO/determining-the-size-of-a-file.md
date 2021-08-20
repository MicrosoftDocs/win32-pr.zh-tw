---
description: GetFileSize 函式會捕獲檔案的大小。
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: 判斷檔案的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf4185d0bb695d73dc3afd03bb1ee7d6fe95cf606960fbdc41c4ce0b33b732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150611"
---
# <a name="determining-the-size-of-a-file"></a>判斷檔案的大小

[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)函式會捕獲檔案的大小。

因為 NTFS 檔案系統的檔案允許在檔案內進行多個資料流程，所以您撰寫來存取檔案的任何應用程式，都必須考慮檔案建立者可以在檔案中包含多個資料流程的可能性。 如果檔案中沒有檢查多個資料流程，應用程式可能會低估檔案的總大小，還有其他錯誤。

 

 



