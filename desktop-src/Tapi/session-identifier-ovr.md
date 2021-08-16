---
description: TAPI 指派每個會話和應用程式都是唯一的會話識別碼。
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: 工作階段識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527706159328b3919e47c39bc5fb160615ed2c202d33c1ce39c711b6921235a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760780"
---
# <a name="session-identifier"></a>工作階段識別碼

TAPI 指派每個會話和應用程式都是唯一的會話識別碼。 應用程式會使用會話識別碼與特定會話相關的 TAPI 進行通訊。 應用程式通常會藉由建立新的通訊會話或 TAPI 提供會話，來取得識別碼。

會話識別碼無法用來將資訊傳遞給另一個應用程式。 基於此目的，請使用服務提供者可能指派的 [呼叫識別碼](call-id-ovr.md)。

如需建立會話並傳回會話識別碼之作業的相關資訊，請參閱 [起始會話](initiate-a-session-ovr.md) 。 如需從 TAPI 取得會話識別碼的作業，請參閱 [回應從其他位置起始的會話](respond-to-session-initiated-elsewhere-ovr.md) 。 如需釋放會話資源的詳細資訊，請參閱 [終止會話](terminate-a-session-ovr.md) 。

所有服務提供者都必須支援某種形式的會話識別碼。

**TAPI 2.x：** 通訊會話的主要識別碼是呼叫控制碼。

**TAPI 3.x：** 會話是由 [呼叫物件](call-object.md) 表示，而主要識別碼是指向 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 介面的指標。

 

 



