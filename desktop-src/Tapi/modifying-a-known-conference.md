---
description: 下列程式碼片段說明如何修改會議時間範圍。 預設的時間範圍是三十分鐘。 在此片段中，時間範圍設定為一年。
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: 修改已知會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191111"
---
# <a name="modifying-a-known-conference"></a>修改已知會議

\[在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

下列程式碼片段說明會議時間範圍的修改。 預設的時間範圍是三十分鐘。 在此片段中，時間範圍設定為一年。

此片段假設已執行 [連接到 ILS 伺服器](connecting-to-an-ils-server.md) ，並已執行 [會議目錄列舉](enumerating-conference-directories.md) 來取得將修改的目錄專案。

此片段也假設這不是多播會議。 變更多播會議的時間需要多播位址佈建服務器的通知。 如需使用多播定址的範例，請參閱取得 [多播位址](acquiring-a-multicast-address.md) 。


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



