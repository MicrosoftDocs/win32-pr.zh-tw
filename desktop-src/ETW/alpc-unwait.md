---
description: 這個類別是 ALPC 結束等候事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: ALPC_Unwait 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512032"
---
# <a name="alpc_unwait-class"></a><span data-ttu-id="dce8d-104">ALPC \_ Unwait 類別</span><span class="sxs-lookup"><span data-stu-id="dce8d-104">ALPC\_Unwait class</span></span>

<span data-ttu-id="dce8d-105">這個類別是 ALPC 結束等候事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="dce8d-105">This class is the event type class for ALPC end wait events.</span></span>

<span data-ttu-id="dce8d-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="dce8d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce8d-107">語法</span><span class="sxs-lookup"><span data-stu-id="dce8d-107">Syntax</span></span>

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="dce8d-108">成員</span><span class="sxs-lookup"><span data-stu-id="dce8d-108">Members</span></span>

<span data-ttu-id="dce8d-109">**ALPC \_ Unwait** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dce8d-109">The **ALPC\_Unwait** class has these types of members:</span></span>

-   [<span data-ttu-id="dce8d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="dce8d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dce8d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dce8d-111">Properties</span></span>

<span data-ttu-id="dce8d-112">**ALPC \_ Unwait** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dce8d-112">The **ALPC\_Unwait** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dce8d-113">**狀態**</span><span class="sxs-lookup"><span data-stu-id="dce8d-113">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce8d-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dce8d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dce8d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dce8d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce8d-116">等候操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="dce8d-116">Status from wait operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dce8d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dce8d-117">Requirements</span></span>



| <span data-ttu-id="dce8d-118">需求</span><span class="sxs-lookup"><span data-stu-id="dce8d-118">Requirement</span></span> | <span data-ttu-id="dce8d-119">值</span><span class="sxs-lookup"><span data-stu-id="dce8d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dce8d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dce8d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dce8d-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dce8d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dce8d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dce8d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dce8d-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dce8d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




