---
description: 與刪除動態實例不同的是，刪除類別是一個簡單的程式。
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: 刪除類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985277"
---
# <a name="deleting-a-class"></a>刪除類別

與刪除動態實例不同的是，刪除類別是一個簡單的程式。 不過，如先前所述，基本或衍生類別很少刪除。 相反地，較常刪除實例。 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)會使用相同的方法來刪除類別物件或實例。 如需詳細資訊，請參閱 [刪除實例](deleting-an-instance.md)。 如需從 WMI 儲存機制移除類別和實例的詳細資訊，請參閱 [**pragma deleteclass**](pragma-deleteclass.md) 預處理器命令。

[適用于 WMI 的 COM API](com-api-for-wmi.md)有不同的方法可刪除實例和刪除物件。

下列程式描述如何刪除基類或衍生類別。

**刪除基類或衍生類別**

-   請呼叫 [**iwbemservices：:D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) 或 [**Iwbemservices：:D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) 方法。

    顧名思義， [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) 會在 [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) 同步刪除實例時，以非同步方式刪除實例。 若要使用 **DeleteClassAsync**，您也必須執行 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。

> [!Note]  
> 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

 

 



