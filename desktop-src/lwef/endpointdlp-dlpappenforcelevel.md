---
description: 指定端點資料遺失防止 (DLP) 作業的強制等級。
title: 'DlpAppEnforceLevel 列舉 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495537"
---
# <a name="dlpappenforcelevel-enumeration"></a><span data-ttu-id="aaa40-103">DlpAppEnforceLevel 列舉</span><span class="sxs-lookup"><span data-stu-id="aaa40-103">DlpAppEnforceLevel enumeration</span></span>

<span data-ttu-id="aaa40-104">指定端點資料遺失防止 (DLP) 作業的強制等級。</span><span class="sxs-lookup"><span data-stu-id="aaa40-104">Specifies the enforcement level of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa40-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaa40-105">Syntax</span></span>


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a><span data-ttu-id="aaa40-106">常數</span><span class="sxs-lookup"><span data-stu-id="aaa40-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aaa40-107">*DlpAppEnforceLevelNone* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaa40-107">*DlpAppEnforceLevelNone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa40-108">應用程式不會強制執行。</span><span class="sxs-lookup"><span data-stu-id="aaa40-108">No enforcement by the app.</span></span> <span data-ttu-id="aaa40-109">DLP 系統將會強制執行此作業。</span><span class="sxs-lookup"><span data-stu-id="aaa40-109">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="aaa40-110">*DlpAppEnforceLevelNotify* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaa40-110">*DlpAppEnforceLevelNotify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa40-111">Tne 應用程式會使用 DLP Api 來通知 DLP 系統有關作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="aaa40-111">Tne app will use the DLP APIs to notify the DLP system about the operation.</span></span> <span data-ttu-id="aaa40-112">DLP 系統將會強制執行此作業。</span><span class="sxs-lookup"><span data-stu-id="aaa40-112">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="aaa40-113">*DlpAppEnforceLevelPrevent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaa40-113">*DlpAppEnforceLevelPrevent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa40-114">目前的版本不支援。</span><span class="sxs-lookup"><span data-stu-id="aaa40-114">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="aaa40-115">*DlpAppEnforceLevelFull* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaa40-115">*DlpAppEnforceLevelFull* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa40-116">目前的版本不支援。</span><span class="sxs-lookup"><span data-stu-id="aaa40-116">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="aaa40-117">*DlpAppEnforceLevelCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaa40-117">*DlpAppEnforceLevelCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa40-118">列舉的最大值。</span><span class="sxs-lookup"><span data-stu-id="aaa40-118">The maximum value of the enumeration.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="aaa40-119">備註</span><span class="sxs-lookup"><span data-stu-id="aaa40-119">Remarks</span></span>

<span data-ttu-id="aaa40-120">[DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md)結構會使用這個列舉的值。</span><span class="sxs-lookup"><span data-stu-id="aaa40-120">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>


## <a name="requirements"></a><span data-ttu-id="aaa40-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaa40-121">Requirements</span></span>



| <span data-ttu-id="aaa40-122">需求</span><span class="sxs-lookup"><span data-stu-id="aaa40-122">Requirement</span></span>          |    <span data-ttu-id="aaa40-123">值</span><span class="sxs-lookup"><span data-stu-id="aaa40-123">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa40-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aaa40-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa40-125">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="aaa40-125">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

