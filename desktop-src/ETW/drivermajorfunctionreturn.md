---
description: 這個類別是驅動程式主要函式呼叫傳回事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: DriverMajorFunctionReturn 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21340224253d1eb3f3ddc733bf2d43e847844282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511012"
---
# <a name="drivermajorfunctionreturn-class"></a><span data-ttu-id="bcbb0-104">DriverMajorFunctionReturn 類別</span><span class="sxs-lookup"><span data-stu-id="bcbb0-104">DriverMajorFunctionReturn class</span></span>

<span data-ttu-id="bcbb0-105">這個類別是驅動程式主要函式呼叫傳回事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="bcbb0-105">This class is the event type class for driver major function call return events.</span></span>

<span data-ttu-id="bcbb0-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="bcbb0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbb0-107">語法</span><span class="sxs-lookup"><span data-stu-id="bcbb0-107">Syntax</span></span>

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="bcbb0-108">成員</span><span class="sxs-lookup"><span data-stu-id="bcbb0-108">Members</span></span>

<span data-ttu-id="bcbb0-109">**DriverMajorFunctionReturn** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bcbb0-109">The **DriverMajorFunctionReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="bcbb0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bcbb0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bcbb0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bcbb0-111">Properties</span></span>

<span data-ttu-id="bcbb0-112">**DriverMajorFunctionReturn** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bcbb0-112">The **DriverMajorFunctionReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bcbb0-113">**Irp**</span><span class="sxs-lookup"><span data-stu-id="bcbb0-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcbb0-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bcbb0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcbb0-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bcbb0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcbb0-116">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="bcbb0-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="bcbb0-117">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="bcbb0-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="bcbb0-118">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="bcbb0-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcbb0-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bcbb0-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcbb0-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bcbb0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcbb0-121">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="bcbb0-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="bcbb0-122">可唯一識別要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcbb0-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="bcbb0-123">您可以使用這個識別碼，將其他驅動程式事件相互關聯，例如 [**DriverCompleteRequest**](drivercompleterequest.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="bcbb0-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcbb0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcbb0-124">Requirements</span></span>



| <span data-ttu-id="bcbb0-125">需求</span><span class="sxs-lookup"><span data-stu-id="bcbb0-125">Requirement</span></span> | <span data-ttu-id="bcbb0-126">值</span><span class="sxs-lookup"><span data-stu-id="bcbb0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bcbb0-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcbb0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbb0-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcbb0-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bcbb0-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcbb0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbb0-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcbb0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcbb0-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcbb0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbb0-132">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="bcbb0-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




