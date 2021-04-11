---
description: 您可以直接呼叫 WSPConnect 來變更預設目的地，即使通訊端已經連接也是一樣。 如果新位址與先前 WSPConnect 中指定的位址不同，則會捨棄任何排入佇列以接收的資料包。
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: 重新連線和中斷連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848753"
---
# <a name="reconnecting-and-disconnecting"></a>重新連線和中斷連接

您可以直接呼叫 [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) 來變更預設目的地，即使通訊端已經連接也是一樣。 如果新位址與先前 **WSPConnect** 中指定的位址不同，則會捨棄任何排入佇列以接收的資料包。

如果為通訊端提供的位址全部為零，則通訊端將會中斷連線，因此， [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) 和 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) 呼叫將會傳回錯誤碼 WSAENOTCONN，不過仍可能使用 [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) 和 [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) 。

 

 
