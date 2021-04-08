---
title: 檔案傳輸一致性
description: BITS 保證根據檔案大小和時間戳記，它所傳輸的檔案版本是一致的，而不是內容 (位無法防止攔截式攻擊) 。
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839360"
---
# <a name="file-transfer-consistency"></a>檔案傳輸一致性

BITS 保證根據檔案大小和時間戳記，它所傳輸的檔案版本是一致的，而不是內容 (位無法防止攔截式攻擊) 。 若要自行驗證內容，您可以使用 [**IBackgroundCopyFile3：： GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) 方法取得包含所下載內容的檔案名，並使用您自己的機制來驗證內容，然後呼叫 [**IBackgroundCopyFile3：： SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) 方法，以指出檔案的內容是否有效。 如果您將驗證狀態設為 **FALSE** ，且內容來自源伺服器，則作業會進入錯誤狀態。 如果內容來自對等，BITS 會從源伺服器下載檔案。

針對下載，如果檔案大小或時間戳記在 BITS 傳輸檔案時變更，BITS 只會重新開機該檔案的傳送。 例如，如果下載作業包含兩個檔案，而且 BITS 正在傳送第二個檔案時，伺服器上的檔案會更新，BITS 只會重新開機第二個檔案的傳送。 第一個已成功傳輸的檔案不會更新，以反映新的變更。

請注意，如果您擁有從伺服器下載的檔案，則應該為檔案的每個新版本建立新的 URL。 如果您針對新版本的檔案使用相同的 URL，部分 proxy 伺服器可能會從其快取中提供過時的資料，因為如果檔案已過時，就不會向源伺服器進行驗證。

針對上傳，如果檔案大小或時間戳記在檔案傳輸期間有所變更，BITS 會產生錯誤，而且作業會處於「BG \_ 工作 \_ 狀態」 \_ 錯誤狀態。

當一或多個使用者要求相同的檔案傳送到相同的位置時，BITS 不會同步處理傳輸要求。 BITS 會分別傳送每個要求的檔案。

 

 




