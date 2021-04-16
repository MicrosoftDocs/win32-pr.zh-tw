---
description: 應用程式可以使用嵌套作業來管理進程的子集。 嵌套作業也可讓使用工作的應用程式裝載其他也使用作業的應用程式。
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: 嵌套作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf105c70ec8e83b395fcce56c6274d4838358bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553761"
---
# <a name="nested-jobs"></a>嵌套作業

應用程式可以使用嵌套作業來管理進程的子集。 嵌套作業也可讓使用工作的應用程式裝載其他也使用作業的應用程式。

**Windows 7、Windows server 2008 R2、WINDOWS XP SP3、Windows server 2008、Windows Vista 和 Windows server 2003：** 進程只能與單一作業相關聯。 內嵌工作是在 Windows 8 和 Windows Server 2012 中引進。

本主題概要說明嵌套作業的作業嵌套和行為：

-   [嵌套作業階層](#nested-job-hierarchies)
-   [建立嵌套作業階層](#creating-a-nested-job-hierarchy)
-   [嵌套作業的作業限制和通知](#job-limits-and-notifications-for-nested-jobs)
-   [嵌套作業的資源帳戶處理](#resource-accounting-for-nested-jobs)
-   [終止嵌套作業](#termination-of-nested-jobs)

如需作業和工作物件的一般資訊，請參閱 [工作物件](job-objects.md)。

## <a name="nested-job-hierarchies"></a>嵌套作業階層

嵌套作業具有父子式關聯性，其中每個子作業都包含其父工作中的處理常式子集。 如果已在作業中的進程已新增至另一個作業，則如果系統可形成有效的作業階層，且這兩個工作集 UI 限制 ([**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) with **JobObjectBasicUIRestrictions**) ，則工作會依預設會進行嵌套。

[圖 1] 顯示的作業階層包含標示為 P0 到 P7 的進程樹狀結構。 作業1是作業2和作業4的 *父工作* ，且是作業 *3 的上* 階。 作業2是作業3的 *直屬父系* ;作業3是工作2的 *直屬子* 系。 作業1、2和3形成 *作業鏈* ，其中的作業1和2是作業3的 *父作業鏈* 。 作業鏈中的結束工作是該作業中進程的 *立即工作* 。 在 [圖 1] 中，作業3是處理 P2、P3 和 P4 的立即工作。

![圖1。 包含進程樹狀結構的嵌套作業階層](images/nested-jobs-a.png)

嵌套作業也可以用來管理對等進程的群組。 在 [圖 2] 所示的作業階層中，作業1是工作2的父工作。 請注意，作業階層可能只包含部分的進程樹狀結構。 在圖2中，P0 不在階層中，但其子進程 P1 至 P5 是。

![[圖 2] 包含對等進程的嵌套作業階層](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>建立嵌套作業階層

作業階層中的進程會使用 [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) 函式明確地與工作物件相關聯，或在進程建立期間隱含關聯，與獨立作業相同。 建立作業和處理常式的順序會決定是否可以建立階層。

若要使用明確關聯建立作業階層，所有工作物件都必須使用 [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)建立，然後您必須針對每個進程多次呼叫 [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) ，才能將進程與其應屬於的每個作業產生關聯。 若要確保作業階層有效，請先將所有進程指派給階層根目錄的工作，然後將進程子集指派給直屬子工作物件，依此類推。 如果以這種順序將進程指派給作業，則在建立階層時，子工作會在其父工作中一律擁有一部分的進程，而這是進行嵌套所需的作業。 如果以隨機順序將進程指派給作業，則子作業在某個時間點會有不在其父工作中的進程。 這是不允許的，因為它會造成 **AssignProcessToJobObject** 失敗。

當進程在進程建立期間以隱含方式與作業相關聯時，子進程會與父進程的作業鏈中的每個作業相關聯。 如果立即工作物件允許 breakaway，子進程會中斷直屬工作物件和父作業鏈中的每個工作，直到階層到達不允許 breakaway 的作業為止。 如果立即工作物件不允許 breakaway，即使父作業鏈中的工作允許，子進程也不會中斷。

## <a name="job-limits-and-notifications-for-nested-jobs"></a>嵌套作業的作業限制和通知

針對某些資源限制，父作業鏈中的作業所設定的限制會決定子工作所強制執行的 *有效限制* 。 子工作的有效限制可以比其父系的限制更嚴格，但不能限制較少。 例如，如果子作業的 priority 類別高於 \_ 一般優先順序類別， \_ \_ 且其父作業的 PRIORITY 類別為一般 \_ 優先順序 \_ 類別，則子工作中處理常式的有效限制為一般 \_ 優先順序 \_ 類別。 但是，如果子工作的 priority 類別低於 \_ 一般 \_ 優先順序 \_ 類別，則子工作中處理常式的有效限制低於 \_ 一般 \_ 優先順序 \_ 類別。 針對優先順序類別、親和性、認可費用、每一進程的執行時間限制、排程類別限制，以及工作集的最小值和最大值，強制執行有效限制。 如需特定資源限制的詳細資訊，請參閱 [ **SetInformationJobObject。**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

當發生特定事件（例如新的進程建立或資源限制違規）時，就會將訊息傳送至與作業相關聯的 i/o 完成通訊埠。 工作也可以註冊，以在超過某些限制時接收通知。 若為非嵌套作業，訊息會傳送至與作業相關聯的 i/o 完成通訊埠。 針對嵌套作業，訊息會傳送至與觸發訊息之作業的父作業鏈中任何作業相關聯的每個 i/o 完成通訊埠。 子工作不需要有相關聯的 i/o 完成通訊埠，就會觸發它所觸發的訊息，以傳送給作業鏈中較高的父工作的 i/o 完成埠。 如需特定訊息的詳細資訊，請參閱 [**JOBOBJECT \_ 關聯 \_ 完成 \_ 埠**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)。

## <a name="resource-accounting-for-nested-jobs"></a>嵌套作業的資源帳戶處理

嵌套作業的資源帳戶處理資訊說明與該工作相關聯之每個進程的使用方式，包括子工作中的處理常式。 因此，作業鏈中的每個工作都代表它自己的進程所使用的匯總資源，以及它在作業鏈底下的每個子工作的處理常式。

## <a name="termination-of-nested-jobs"></a>終止嵌套作業

當作業階層中的作業終止時，系統會終止該作業中的進程及其所有子工作，從階層底部的子工作開始。 每個終止的進程所使用的未處理資源會收取父工作的費用。

工作控制碼必須有工作 \_ 物件 \_ 終止存取權，與獨立作業的存取權相同。

 

 
