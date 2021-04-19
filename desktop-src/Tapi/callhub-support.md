---
description: CallHub 追蹤是 TAPI 3.0 版中的新功能。
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: CallHub 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987677"
---
# <a name="callhub-support"></a>CallHub 支援

CallHub 追蹤是 TAPI 3.0 版中的新功能。 CallHub 功能已新增至 TAPI 2.1 程式設計項目，並提供 Windows 2000。 *CallHub* 代表呼叫的協力廠商觀點，而 TAPI 的呼叫控制碼則代表來電的第一方觀點。 使用 CallHub 追蹤時，會要求服務提供者遵循 CallHubs，並在 CallHub 的存留期內提供呼叫的相關資訊。 當新的當事人加入並離開 CallHub 時，服務提供者應該告知 TAPI。

服務提供者不需要執行任何新的函數，就能支援 CallHub。 它只需要填入 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)結構的 **dwCallID** 成員。 在 TAPI 3 中，TAPI 會收集所有具有相同 **dwCallID** 的呼叫，並建立應用程式可用來追蹤通話的 CallHub 控制碼。

 

 
