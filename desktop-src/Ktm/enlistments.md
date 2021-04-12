---
description: 當資源管理員開始參與該特定交易時，會在交易中登記。
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: 登記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52820af2a7b280bc4740d0309fb627725e648685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194952"
---
# <a name="enlistments"></a>登記

當資源管理員開始參與該特定交易時，會在交易中登記。 登記會定義資源管理員所接受的通知。 當資源管理員在交易中登記時，會建立一個登錄物件。 此物件會向 KTM 指出資源管理員 (RM) 正在要求有關指定交易的通知。

RM 會提供 [**通知 \_ 遮罩**](notification-mask.md) 結構，以詳細說明其要求的通知。

## <a name="enlistment-functions"></a>登記函數

下列函式可用於登記。



| 函式                                                                          | 描述                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | 指出資源管理員 (RM) 已完成認可交易管理員 (TM) 所要求的交易。                                                                                                                                                                                                                                                                        |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | 建立登記、設定其初始狀態，並使用指定的存取權開啟登記的控制碼。                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | 從 KTM 抓取修復資料的不透明結構。 藉由呼叫 [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) 函式，可代表資源管理員將復原資訊儲存在記錄檔中， (RM) 。 失敗之後，RM 可以使用 [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) 函式來取得資訊。 |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | 開啟現有的登錄物件，並將控制碼傳回給登記。                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | 要求將指定的登記轉換成隻讀登記。 唯讀登記無法參與交易的結果，也不會永久記錄以進行復原。                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | 復原與登記相關聯的指定交易。 無法針對唯讀登記呼叫此函數。                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | 從 KTM 設定不透明、使用者定義的修復資料結構。 藉由呼叫 [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)，可代表資源管理員將復原資訊儲存在記錄檔中， (RM) 。 失敗之後，RM 可以使用 [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) 來取得資訊。                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | 指出資源管理員 (RM) 拒絕單一階段要求。 當交易管理員 (TM) 收到此呼叫時，它會起始兩階段認可，並將準備要求傳送到所有已登錄的 RMs。                                                                                                                                                                                       |



 

 

 



