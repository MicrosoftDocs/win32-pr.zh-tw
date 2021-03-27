---
description: 此類別是 ALPC 等候回復事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: ALPC_Wait_For_Reply 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 898077511db25ec7f53bc075ecb845d04e540626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972237"
---
# <a name="alpc_wait_for_reply-class"></a><span data-ttu-id="bf9ab-104">ALPC \_ 等候 \_ \_ 回復類別</span><span class="sxs-lookup"><span data-stu-id="bf9ab-104">ALPC\_Wait\_For\_Reply class</span></span>

<span data-ttu-id="bf9ab-105">此類別是 ALPC 等候回復事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="bf9ab-105">This class is the event type class for ALPC wait for reply events.</span></span>

<span data-ttu-id="bf9ab-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="bf9ab-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9ab-107">語法</span><span class="sxs-lookup"><span data-stu-id="bf9ab-107">Syntax</span></span>

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="bf9ab-108">成員</span><span class="sxs-lookup"><span data-stu-id="bf9ab-108">Members</span></span>

<span data-ttu-id="bf9ab-109">**ALPC \_ 等候 \_ \_ 回復** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bf9ab-109">The **ALPC\_Wait\_For\_Reply** class has these types of members:</span></span>

-   [<span data-ttu-id="bf9ab-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bf9ab-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf9ab-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bf9ab-111">Properties</span></span>

<span data-ttu-id="bf9ab-112">**ALPC \_ 等候 \_ \_ 回復** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bf9ab-112">The **ALPC\_Wait\_For\_Reply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf9ab-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="bf9ab-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf9ab-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf9ab-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf9ab-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf9ab-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf9ab-116">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf9ab-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf9ab-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf9ab-117">Requirements</span></span>



| <span data-ttu-id="bf9ab-118">需求</span><span class="sxs-lookup"><span data-stu-id="bf9ab-118">Requirement</span></span> | <span data-ttu-id="bf9ab-119">值</span><span class="sxs-lookup"><span data-stu-id="bf9ab-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf9ab-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf9ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf9ab-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf9ab-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bf9ab-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf9ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf9ab-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf9ab-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




