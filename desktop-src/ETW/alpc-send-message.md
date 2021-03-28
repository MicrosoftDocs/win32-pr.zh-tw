---
description: 這個類別是 ALPC 傳送訊息事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: ALPC_Send_Message 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113892"
---
# <a name="alpc_send_message-class"></a><span data-ttu-id="1097c-104">ALPC \_ 傳送 \_ 訊息類別</span><span class="sxs-lookup"><span data-stu-id="1097c-104">ALPC\_Send\_Message class</span></span>

<span data-ttu-id="1097c-105">這個類別是 ALPC 傳送訊息事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="1097c-105">This class is the event type class for ALPC send message events.</span></span>

<span data-ttu-id="1097c-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="1097c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1097c-107">語法</span><span class="sxs-lookup"><span data-stu-id="1097c-107">Syntax</span></span>

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="1097c-108">成員</span><span class="sxs-lookup"><span data-stu-id="1097c-108">Members</span></span>

<span data-ttu-id="1097c-109">**ALPC \_ 傳送 \_ 訊息** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1097c-109">The **ALPC\_Send\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="1097c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1097c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1097c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1097c-111">Properties</span></span>

<span data-ttu-id="1097c-112">**ALPC \_ 傳送 \_ 訊息** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1097c-112">The **ALPC\_Send\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1097c-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="1097c-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1097c-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1097c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1097c-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1097c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1097c-116">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="1097c-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1097c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1097c-117">Requirements</span></span>



| <span data-ttu-id="1097c-118">需求</span><span class="sxs-lookup"><span data-stu-id="1097c-118">Requirement</span></span> | <span data-ttu-id="1097c-119">值</span><span class="sxs-lookup"><span data-stu-id="1097c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1097c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1097c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1097c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1097c-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1097c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1097c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1097c-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1097c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




