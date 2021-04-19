---
description: 指定端點資料遺失防止 (DLP) 操作的動作類型。
title: 'DlpActionType 列舉 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495538"
---
# <a name="dlpactiontype-enumeration"></a><span data-ttu-id="5f793-103">DlpActionType 列舉</span><span class="sxs-lookup"><span data-stu-id="5f793-103">DlpActionType enumeration</span></span>

<span data-ttu-id="5f793-104">指定端點資料遺失防止 (DLP) 操作的動作類型。</span><span class="sxs-lookup"><span data-stu-id="5f793-104">Specifies the action type of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f793-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f793-105">Syntax</span></span>


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a><span data-ttu-id="5f793-106">常數</span><span class="sxs-lookup"><span data-stu-id="5f793-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5f793-107">*DlpActionTypeCopyToRemovableMedia*</span><span class="sxs-lookup"><span data-stu-id="5f793-107">*DlpActionTypeCopyToRemovableMedia*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-108">卸載式媒體的複製操作。</span><span class="sxs-lookup"><span data-stu-id="5f793-108">A copy operation to removable media.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5f793-109">*DlpActionTypeCopyToNetworkShare*</span><span class="sxs-lookup"><span data-stu-id="5f793-109">*DlpActionTypeCopyToNetworkShare*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-110">共用網路資料夾的複製操作。</span><span class="sxs-lookup"><span data-stu-id="5f793-110">A copy operation to a shared network folder.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5f793-111">*DlpActionTypeCopyToClipboard*</span><span class="sxs-lookup"><span data-stu-id="5f793-111">*DlpActionTypeCopyToClipboard*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-112">剪貼簿的複製操作。</span><span class="sxs-lookup"><span data-stu-id="5f793-112">A copy operation to the clipboard.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5f793-113">*DlpActionTypePrint*</span><span class="sxs-lookup"><span data-stu-id="5f793-113">*DlpActionTypePrint*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-114">列印操作。</span><span class="sxs-lookup"><span data-stu-id="5f793-114">A print operation.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="5f793-115">*DlpActionTypeScreenClip*</span><span class="sxs-lookup"><span data-stu-id="5f793-115">*DlpActionTypeScreenClip*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-116">畫面捕捉作業。</span><span class="sxs-lookup"><span data-stu-id="5f793-116">A screen capture operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5f793-117">*DlpActionTypeAccessByUnallowedApp*</span><span class="sxs-lookup"><span data-stu-id="5f793-117">*DlpActionTypeAccessByUnallowedApp*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-118">不允許之應用程式所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="5f793-118">An operation performed by an unallowed app.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="5f793-119">*DlpActionTypeCloudAppEgress*</span><span class="sxs-lookup"><span data-stu-id="5f793-119">*DlpActionTypeCloudAppEgress*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-120">以雲端位置為目標的作業。</span><span class="sxs-lookup"><span data-stu-id="5f793-120">An operation targeted to a cloud location.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5f793-121">*DlpActionTypeAccessByBluetoothApp*</span><span class="sxs-lookup"><span data-stu-id="5f793-121">*DlpActionTypeAccessByBluetoothApp*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-122">包含藍牙應用程式存取權的作業。</span><span class="sxs-lookup"><span data-stu-id="5f793-122">An operation that includes access by a bluetooth app.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5f793-123">*DlpActionTypeAccessByRDPApp*</span><span class="sxs-lookup"><span data-stu-id="5f793-123">*DlpActionTypeAccessByRDPApp*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-124">包含遠端桌面存取權的作業。</span><span class="sxs-lookup"><span data-stu-id="5f793-124">An operation that includes access by a remote desktop.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5f793-125">*DlpActionTypeCount*</span><span class="sxs-lookup"><span data-stu-id="5f793-125">*DlpActionTypeCount*</span></span>
</dt> <dd>

<span data-ttu-id="5f793-126">列舉的最大值。</span><span class="sxs-lookup"><span data-stu-id="5f793-126">The maximum value of the enumeration.</span></span>

</dd> </dl>
 

## <a name="remarks"></a><span data-ttu-id="5f793-127">備註</span><span class="sxs-lookup"><span data-stu-id="5f793-127">Remarks</span></span>

<span data-ttu-id="5f793-128">[DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md)結構會使用這個列舉的值。</span><span class="sxs-lookup"><span data-stu-id="5f793-128">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f793-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f793-129">Requirements</span></span>



| <span data-ttu-id="5f793-130">需求</span><span class="sxs-lookup"><span data-stu-id="5f793-130">Requirement</span></span>          |    <span data-ttu-id="5f793-131">值</span><span class="sxs-lookup"><span data-stu-id="5f793-131">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f793-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f793-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5f793-133">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="5f793-133">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

