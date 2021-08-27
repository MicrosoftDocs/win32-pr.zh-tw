---
description: 如果您要撰寫服務或元件，且需要使用交易式服務，或者，如果您需要監視核心交易的狀態，您需要建立資源管理員 (RM) 。
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: 撰寫 Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b1443bef61f56a14779612a6275aacbd65e344d7294325bd87b953795f0f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086448"
---
# <a name="writing-a-resource-manager"></a>撰寫 Resource Manager

如果您要撰寫服務或元件，且需要使用交易式服務，或者，如果您需要監視核心交易的狀態，您需要建立資源管理員 (RM) 。

若要撰寫 resource manager，您必須建立多個核心物件。 RM 使用的物件為：

-   交易管理員 (TM) 物件
-   Resource Manager 物件
-   登錄物件

首先，建立 TM 物件。 有兩種類型的 Tm：

-   Volatile-這些 Tm 沒有記錄檔，無法復原其狀態
-   耐用–這些 Tm 有記錄檔

若要建立耐用 TM，您必須建立 CLFS 記錄檔並呼叫 [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) ，或讓 KTM 為您建立。 建立耐用 TM 之後，您必須先呼叫 [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)來復原 tm。 在 TM 復原之後，就可以使用它。

如果您已復原現有的 TM，所有與此 TM 相關聯的 RMs 都會開始接收修復訊息。 如需詳細資訊，請參閱復原 [處理](recovery-processing.md)。

接下來，您會使用 TM 控制碼呼叫 [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) 來建立資源管理員。 RM 可以是暫時性或耐用的。 只有持久的 Tm 可以搭配永久性的 RMs 使用。

以交易方式工作時，您可以藉由呼叫 [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)並指定要接收的通知，在交易中登記。

**注意**  您可以在呼叫 [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) 完成之前，開始接收通知。

當您收到通知時，請 \* 在與處理通知相關聯的任何工作完成時，呼叫適當的「完成」功能。 完整的功能包括：

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

如果資源管理員在任何時候無法完成交易的工作，或如果繼續，則會導致應用程式無法復原在交易內完成的工作，您必須呼叫 [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)來回複交易。

 

 



