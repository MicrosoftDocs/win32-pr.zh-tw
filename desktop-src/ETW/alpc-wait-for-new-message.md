---
description: 此類別是 ALPC 等候新訊息事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: ALPC_Wait_For_New_Message 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75cbda11a2a27eec811f8ff47966d12c6a86cf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972240"
---
# <a name="alpc_wait_for_new_message-class"></a><span data-ttu-id="b8a6f-104">ALPC \_ 等候 \_ \_ 新的 \_ 訊息類別</span><span class="sxs-lookup"><span data-stu-id="b8a6f-104">ALPC\_Wait\_For\_New\_Message class</span></span>

<span data-ttu-id="b8a6f-105">此類別是 ALPC 等候新訊息事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="b8a6f-105">This class is the event type class for ALPC wait for new message events.</span></span>

<span data-ttu-id="b8a6f-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="b8a6f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a6f-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8a6f-107">Syntax</span></span>

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a><span data-ttu-id="b8a6f-108">成員</span><span class="sxs-lookup"><span data-stu-id="b8a6f-108">Members</span></span>

<span data-ttu-id="b8a6f-109">**ALPC \_ 等候 \_ 新的 \_ \_ 訊息** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b8a6f-109">The **ALPC\_Wait\_For\_New\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="b8a6f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b8a6f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8a6f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b8a6f-111">Properties</span></span>

<span data-ttu-id="b8a6f-112">**ALPC \_ 等候 \_ 新的 \_ \_ 訊息** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b8a6f-112">The **ALPC\_Wait\_For\_New\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8a6f-113">**IsServerPort**</span><span class="sxs-lookup"><span data-stu-id="b8a6f-113">**IsServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a6f-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b8a6f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8a6f-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a6f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a6f-116">指出埠是否為伺服器埠。</span><span class="sxs-lookup"><span data-stu-id="b8a6f-116">Indicates if the port is a server port.</span></span>

</dd> <dt>

<span data-ttu-id="b8a6f-117">**PortName**</span><span class="sxs-lookup"><span data-stu-id="b8a6f-117">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a6f-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a6f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a6f-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a6f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a6f-120">字串，其中包含正在等候 ALPC 的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a6f-120">String that contains the name of the port on which ALPC is waiting.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8a6f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8a6f-121">Requirements</span></span>



| <span data-ttu-id="b8a6f-122">需求</span><span class="sxs-lookup"><span data-stu-id="b8a6f-122">Requirement</span></span> | <span data-ttu-id="b8a6f-123">值</span><span class="sxs-lookup"><span data-stu-id="b8a6f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8a6f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8a6f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a6f-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8a6f-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8a6f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8a6f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a6f-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8a6f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




