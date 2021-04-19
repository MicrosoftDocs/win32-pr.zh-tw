---
description: 呼叫物件代表本機位址與一或多個其他位址之間的位址連接。
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: 呼叫物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980097"
---
# <a name="call-object"></a>呼叫物件

呼叫物件代表位址在本機位址與一或多個其他位址之間的連接。 所有呼叫控制都是透過呼叫物件來完成。 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) 和 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 是呼叫物件上最常使用的介面。 這些介面會執行各種不同的作業和查詢，例如取得媒體資料流程的介面指標或取得呼叫者識別碼。 請參閱有關 [會話作業](session-operations-ovr.md) 和 [會話資訊](session-information-ovr.md) 的主要總覽章節，以查看 TAPI 所支援的作業。

媒體服務提供者可以執行由 TAPI 在呼叫物件上匯總的 [提供者特定介面](provider-specific-interfaces.md)。 如需提供者所執行之功能的詳細資訊，請參閱服務提供者的檔。

[進行呼叫](make-a-call.md)和[接收呼叫](receive-a-call.md)程式碼範例會顯示使用呼叫物件的一些圖例。

請參閱 [呼叫物件介面](call-object-interfaces.md) ，以取得與呼叫物件相關聯之所有介面的清單。

 

 



