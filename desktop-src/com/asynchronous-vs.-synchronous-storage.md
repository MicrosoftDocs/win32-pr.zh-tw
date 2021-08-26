---
title: 非同步和同步儲存體
description: 非同步和同步儲存體
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5662f5d9291de19fb39f044731ed72fd1db2cb04fe29d76eb785981ddeb8a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071088"
---
# <a name="asynchronous-and-synchronous-storage"></a>非同步和同步儲存體

非同步標記也可能會在 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))通知中傳回 [非同步儲存體](/windows/desktop/Stg/asynchronous-storage)物件。 當系結仍在進行時，這個儲存物件可能會允許存取某些物件的持續性資料。 用戶端可以選擇兩種儲存模式：封鎖和非封鎖。

在封鎖模式中，如果資料無法使用，則呼叫會封鎖，直到資料到達為止。 在非封鎖模式中，儲存物件不會封鎖呼叫，而是在 \_ 資料無法使用時，傳回新的錯誤 E。 用戶端注意到非同步系結和儲存體會記下此錯誤，並等候進一步的通知 ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) 重試作業。 用戶端可以選擇是否要 \_ 在傳回 [**IBindStatusCallback：： GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))的 *GRFBINDF* 值中設定 BINDF ASYNCSTORAGE 旗標，以在同步 (封鎖) 和非同步 (非封鎖) 儲存體之間選擇。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步名字](asynchronous-monikers.md)
</dt> </dl>

 

 