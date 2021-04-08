---
description: TSPIMessage 是一種列舉型別，可定義 TSPI 中未出現在 TAPI 中的額外 LINEEVENT 和 PHONEEVENT 函式集合。
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691536"
---
# <a name="tspimessage"></a>TSPIMessage

**TSPIMessage** 是一種列舉型別，可定義 TSPI 中未出現在 TAPI 中的額外 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 和 [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) 函式集合。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI \_ 訊息 \_ 基底
</dt> <dd>

TSPI 特定訊息值範圍中的最小數位。 這個值本身並沒有任何意義，而是做為定義其他值的基底。

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>行 \_ NEWCALL
</dt> <dd>

指定新的連入呼叫已抵達，並將其引進至 TAPI。 這必須是第一個傳送至 TAPI 的訊息，以進行新的連入呼叫。 TAPI 在處理此訊息時，會傳回它的不透明識別碼作為呼叫的一部分。

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>行 \_ CALLDEVSPECIFIC
</dt> <dd>

指定在通話裝置上發生裝置特定事件。

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>行 \_ CALLDEVSPECIFICFEATURE
</dt> <dd>

指定在通話裝置上發生裝置特定的功能事件。

</dd> </dl>

 

 
