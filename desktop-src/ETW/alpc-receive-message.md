---
description: 這個類別是 ALPC 接收訊息事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: ALPC_Receive_Message 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972245"
---
# <a name="alpc_receive_message-class"></a><span data-ttu-id="2670a-104">ALPC \_ Receive \_ Message 類別</span><span class="sxs-lookup"><span data-stu-id="2670a-104">ALPC\_Receive\_Message class</span></span>

<span data-ttu-id="2670a-105">這個類別是 ALPC 接收訊息事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="2670a-105">This class is the event type class for ALPC receive message events.</span></span>

<span data-ttu-id="2670a-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="2670a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2670a-107">語法</span><span class="sxs-lookup"><span data-stu-id="2670a-107">Syntax</span></span>

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="2670a-108">成員</span><span class="sxs-lookup"><span data-stu-id="2670a-108">Members</span></span>

<span data-ttu-id="2670a-109">**ALPC \_ Receive \_ Message** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2670a-109">The **ALPC\_Receive\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="2670a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2670a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2670a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2670a-111">Properties</span></span>

<span data-ttu-id="2670a-112">**ALPC \_ Receive \_ Message** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2670a-112">The **ALPC\_Receive\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2670a-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="2670a-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2670a-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2670a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2670a-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2670a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2670a-116">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="2670a-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2670a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2670a-117">Requirements</span></span>



| <span data-ttu-id="2670a-118">需求</span><span class="sxs-lookup"><span data-stu-id="2670a-118">Requirement</span></span> | <span data-ttu-id="2670a-119">值</span><span class="sxs-lookup"><span data-stu-id="2670a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2670a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2670a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2670a-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2670a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2670a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2670a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2670a-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2670a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




