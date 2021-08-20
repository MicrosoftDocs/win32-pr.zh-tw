---
description: 強制使用者設定檔是一種特殊的預先設定漫遊使用者設定檔，可讓系統管理員用來指定使用者的設定。
title: 強制使用者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 748135affd0b6be399242ff171c88a45da3047911f0603f47eccf0a1f0ba0018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678142"
---
# <a name="mandatory-user-profiles"></a>強制使用者設定檔

強制使用者設定檔是一種特殊的預先設定 [漫遊使用者設定檔](roaming-user-profiles.md) ，可讓系統管理員用來指定使用者的設定。 使用強制使用者設定檔時，使用者可以修改其桌面，但當使用者登出時，不會儲存變更。 使用者下一次登入時，系統會下載系統管理員所建立的強制使用者設定檔。 強制設定檔有兩種類型： *標準強制* 設定檔和 *超級強制* 設定檔。

當系統管理員將伺服器上的 Ntuser.man 登錄區)  (登錄 hive 時，使用者設定檔會變成強制設定檔，以 Ntuser.man。 Man 延伸會使使用者設定檔成為唯讀設定檔。

當設定檔路徑的資料夾名稱結束時，使用者設定檔會變成 *超級強制性*。例如， \\ \\ server \\ share \\ mandatoryprofile。 \\

超級強制使用者設定檔類似于一般的強制設定檔，例外狀況是當儲存強制設定檔的伺服器無法使用時，具有超級強制設定檔的使用者無法登入。 具有一般強制設定檔的使用者可以使用強制設定檔的本機快取複本來登入。

只有系統管理員可以對強制使用者設定檔進行變更。

 

 



