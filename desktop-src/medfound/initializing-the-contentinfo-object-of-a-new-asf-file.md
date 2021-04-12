---
description: 初始化新 ASF 檔案的 ContentInfo 物件
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: 初始化新 ASF 檔案的 ContentInfo 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74826942700f4be8028075fcd9466414834eb8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318308"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>初始化新 ASF 檔案的 ContentInfo 物件

藉由呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 函式來建立空的 ContentInfo 物件之後，應用程式必須呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) 以提供編碼設定檔。 如需建立設定檔的詳細資訊，請參閱 [建立 ASF 設定檔](creating-an-asf-profile.md)。

從設定檔讀取資訊之前， **SetProfile** 方法必須藉由檢查資料流程識別碼或媒體類型來驗證指定的設定檔物件。 如果設定檔通過驗證，則會產生不同的標頭物件，例如檔案屬性物件、資料流程位元速率屬性物件、資料流程屬性物件，以及相互排除物件。

**SetProfile** 會計算並設定某些屬性的建議值，例如預先設定的值。 如果尚未設定此值，建議的預先計算值（以毫秒為單位）取決於設定檔中針對資料流程所指定之有漏洞 bucket 的最大緩衝區視窗。 同樣地，也會設定最小和最大的資料封包大小。 建議的值可能會覆寫透過屬性在設定檔上設定的封包大小。

因為檔案正在建立中，所以檔案會分類為廣播類型，並以檔案屬性物件的 [旗標] 欄位表示。 某些未知值（例如資料封包數、播放持續時間和傳送持續時間）會設定為零。 這些值是由 **MF \_ PD \_ ASF \_ xxx** 屬性工作表示，而且必須在檔案建立完成之後，由應用程式更新。

指定的設定檔物件會取代任何與 ContentInfo 物件相關聯的現有設定檔、移除參考的標頭物件，以及重設通用檔案屬性，例如預先處理和資料封包大小。

**SetProfile** 方法也會建立代表 ASF 資料物件的資料物件。 如果您重複使用 ContentInfo 物件，其中包含任何資料封包的相關資訊，則 **SetProfile** 會失敗，並傳回 MF \_ E \_ 已 \_ 初始化的錯誤，指出它已與現有的 ASF 資料物件相關聯。 根據預設，對於新的 ContentInfo 物件，資料封包計數會設定為零，而且資料物件大小會設定為50個位元組。 如果您使用多工器來產生資料封包，則多工器會更新 ContentInfo 物件，以反映新的值，例如資料封包計數。 如需有關產生資料封包的詳細資訊，請參閱 [產生新的 ASF 資料封包](generating-new-asf-data-packets.md)。

將所有的標頭物件加入到最後一個 ASF 標頭物件之後，就可以藉由呼叫 [**IMFASFContentInfo：： GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize)來取出總標頭大小。 此大小包含初始資料物件大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 ContentInfo 物件中設定屬性](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[為新檔案撰寫 ASF 標頭物件](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



