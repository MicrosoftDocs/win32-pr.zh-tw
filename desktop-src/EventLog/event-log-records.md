---
description: 每個事件的相關資訊會儲存在事件記錄檔的事件記錄檔中。 事件記錄檔記錄包含時間、類型和類別資訊。 如需詳細資訊，請參閱 EVENTLOGRECORD 結構。
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: 事件記錄檔記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848856"
---
# <a name="event-log-records"></a>事件記錄檔記錄

每個事件的相關資訊會儲存 *在事件記錄* 檔的事件記錄檔中。 事件記錄檔記錄包含時間、類型和類別資訊。 如需詳細資訊，請參閱 [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) 結構。

[**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord)的 **RecordNumber** 成員包含事件記錄檔記錄的記錄號碼。 寫入事件記錄檔的第一筆記錄是記錄號碼1，而其他記錄則會依序編號。 如果記錄號碼達到 ULONG 的 \_ 最大值，下一個記錄號碼將是0，而不是 1; 不過，您可以使用零來搜尋記錄。

如果 [保留](eventlog-key.md) 登錄值設定為零，當達到記錄檔大小上限時，就會覆寫事件記錄。 因此，事件記錄檔中最舊的記錄可能不會記錄號碼1。 若要識別記錄檔中最舊的記錄，請呼叫 [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) 函數。 然後，您可以呼叫 [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) 函式，並將傳回的值加入最舊的記錄號碼，以判斷最新的記錄。

您可以使用 [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) 函數，從事件記錄檔讀取個別記錄。 如需詳細資訊，請參閱 [查詢事件資訊](querying-for-event-source-messages.md)。

 

 



