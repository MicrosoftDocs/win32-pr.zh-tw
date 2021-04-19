---
description: 會話終止可能源自于使用者要求、由另一方遠端中斷連接，或因應用程式特定的原因而產生。
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: 終止會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981707"
---
# <a name="terminate-a-session"></a>終止會話

會話終止可能源自于使用者要求、由另一方遠端中斷連接，或因應用程式特定的原因而產生。 當會話結束時， [會話識別碼](session-identifier-ovr.md) 會維持有效，直到特別發行，而且可用來收集連線後資料。

解除配置和釋放與會話相關聯的資源，即可完成會話終止。 如果會話只是卸載或中斷連線，但是未釋出資源，則結果是應用程式中的記憶體流失，也可能是在服務提供者中。

**TAPI 2.x：** 請參閱 [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop)、 [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall)。

**TAPI 3.x：** 請參閱 [**ITBasicCallControl：:D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)，在 Call 物件指標上執行標準 COM 版本。

 

 
