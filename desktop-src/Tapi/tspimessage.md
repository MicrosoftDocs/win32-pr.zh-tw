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
# <a name="tspimessage"></a><span data-ttu-id="5aeeb-103">TSPIMessage</span><span class="sxs-lookup"><span data-stu-id="5aeeb-103">TSPIMessage</span></span>

<span data-ttu-id="5aeeb-104">**TSPIMessage** 是一種列舉型別，可定義 TSPI 中未出現在 TAPI 中的額外 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 和 [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) 函式集合。</span><span class="sxs-lookup"><span data-stu-id="5aeeb-104">**TSPIMessage** is an enumeration type that defines the set of additional [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) and [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) functions appearing in TSPI that do not appear in TAPI.</span></span>

## <a name="parameters"></a><span data-ttu-id="5aeeb-105">參數</span><span class="sxs-lookup"><span data-stu-id="5aeeb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aeeb-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI \_ 訊息 \_ 基底</span><span class="sxs-lookup"><span data-stu-id="5aeeb-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI\_MESSAGE\_BASE</span></span>
</dt> <dd>

<span data-ttu-id="5aeeb-107">TSPI 特定訊息值範圍中的最小數位。</span><span class="sxs-lookup"><span data-stu-id="5aeeb-107">The lowest number in the range of TSPI-specific message values.</span></span> <span data-ttu-id="5aeeb-108">這個值本身並沒有任何意義，而是做為定義其他值的基底。</span><span class="sxs-lookup"><span data-stu-id="5aeeb-108">This value has no meaning by itself, but serves as a base for defining the other values.</span></span>

</dd> <dt>

<span data-ttu-id="5aeeb-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>行 \_ NEWCALL</span><span class="sxs-lookup"><span data-stu-id="5aeeb-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE\_NEWCALL</span></span>
</dt> <dd>

<span data-ttu-id="5aeeb-110">指定新的連入呼叫已抵達，並將其引進至 TAPI。</span><span class="sxs-lookup"><span data-stu-id="5aeeb-110">Specifies that a new, incoming call has arrived and introduces it to TAPI.</span></span> <span data-ttu-id="5aeeb-111">這必須是第一個傳送至 TAPI 的訊息，以進行新的連入呼叫。</span><span class="sxs-lookup"><span data-stu-id="5aeeb-111">This must be the first message sent to TAPI for a new incoming call.</span></span> <span data-ttu-id="5aeeb-112">TAPI 在處理此訊息時，會傳回它的不透明識別碼作為呼叫的一部分。</span><span class="sxs-lookup"><span data-stu-id="5aeeb-112">TAPI returns its opaque identifier for the call as part of its handling of this message.</span></span>

</dd> <dt>

<span data-ttu-id="5aeeb-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>行 \_ CALLDEVSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="5aeeb-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE\_CALLDEVSPECIFIC</span></span>
</dt> <dd>

<span data-ttu-id="5aeeb-114">指定在通話裝置上發生裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="5aeeb-114">Specifies that a device-specific event has occurred on a call device.</span></span>

</dd> <dt>

<span data-ttu-id="5aeeb-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>行 \_ CALLDEVSPECIFICFEATURE</span><span class="sxs-lookup"><span data-stu-id="5aeeb-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE\_CALLDEVSPECIFICFEATURE</span></span>
</dt> <dd>

<span data-ttu-id="5aeeb-116">指定在通話裝置上發生裝置特定的功能事件。</span><span class="sxs-lookup"><span data-stu-id="5aeeb-116">Specifies that a device-specific feature event has occurred on a call device.</span></span>

</dd> </dl>

 

 
