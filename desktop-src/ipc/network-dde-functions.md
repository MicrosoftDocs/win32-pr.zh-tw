---
description: 下列函式用於網路 DDE。
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: 網路 DDE 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b37e83dd6b335e1acd2e77010fa61d0da5e3e26af5b46eef54d5ee20cf2eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756307"
---
# <a name="network-dde-functions"></a>網路 DDE 函數

\[不再支援網路 DDE。 Nddeapi.dll 存在於 Windows Vista 中，但所有的函式呼叫會傳回 NDDE \_ 未 \_ 執行。\]

下列函式用於網路 DDE。



| 函式                                                   | 描述                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | 將網路 DDE 函數所傳回的錯誤碼轉換成錯誤字串，以說明傳回的錯誤碼。 |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | 抓取與 DDE 共用相關聯的安全描述項。                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | 抓取與在伺服器使用者的受信任共用清單中之 DDE 共用相關聯的選項。                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | 判斷應用程式和主題字串 ( "*AppName* \| *TopicName*" ) 是否使用適當的語法。                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | 判斷共用名稱是否使用適當的語法。                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | 設定與 DDE 共用相關聯的安全描述項。                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | 在目前使用者的內容中，授與指定的 DDE 共用信任狀態。                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | 建立新的 DDE 共用，並將其新增至 DDE 共用資料庫管理員 (DSDM) 。                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | 從 DSDM 中刪除 DDE 共用。                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | 抓取可用的 DDE 共用清單。                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | 捕獲 DDE 共用資訊。                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | 設定 DDE 共用資訊。                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | 抓取呼叫進程內容中受信任之所有網路 DDE 共用的名稱。                 |



 

 

 



