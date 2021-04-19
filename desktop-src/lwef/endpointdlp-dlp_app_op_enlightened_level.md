---
description: 使端點資料遺失防止 (DLP) 動作與強制等級產生關聯。
title: 'DLP_APP_OP_ENLIGHTENED_LEVEL 結構 (endpointdlp .h) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495545"
---
# <a name="dlp_app_op_enlightened_level-structure"></a><span data-ttu-id="ee8f8-103">DLP_APP_OP_ENLIGHTENED_LEVEL 結構</span><span class="sxs-lookup"><span data-stu-id="ee8f8-103">DLP_APP_OP_ENLIGHTENED_LEVEL structure</span></span>

<span data-ttu-id="ee8f8-104">使端點資料遺失防止 (DLP) 動作與強制等級產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ee8f8-104">Associates an endpoint Data Loss Prevention (DLP) action with an enforcement level.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8f8-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee8f8-105">Syntax</span></span>


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a><span data-ttu-id="ee8f8-106">成員</span><span class="sxs-lookup"><span data-stu-id="ee8f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee8f8-107">*操作* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee8f8-107">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8f8-108">[DlpActionType](endpointdlp-dlpactiontype.md)列舉中的值，指定端點 DLP 動作類型。</span><span class="sxs-lookup"><span data-stu-id="ee8f8-108">A value from the [DlpActionType](endpointdlp-dlpactiontype.md) enumeration specifying the endpoint DLP action type.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="ee8f8-109">*AppEnforcementLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee8f8-109">*AppEnforcementLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8f8-110">[DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md)中的值，指定相關聯之端點 DLP 動作類型的強制執行層級。</span><span class="sxs-lookup"><span data-stu-id="ee8f8-110">A value from the [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) specifying the level of enforcement for the associated endpoint DLP action type.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="ee8f8-111">備註</span><span class="sxs-lookup"><span data-stu-id="ee8f8-111">Remarks</span></span>

<span data-ttu-id="ee8f8-112">將這些結構的陣列傳遞至 [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) ，以設定一組端點 DLP 作業的強制模式。</span><span class="sxs-lookup"><span data-stu-id="ee8f8-112">Pass an array of these structures into [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) to set the enforcement mode for a set of endpoint DLP operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8f8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee8f8-113">Requirements</span></span>



| <span data-ttu-id="ee8f8-114">需求</span><span class="sxs-lookup"><span data-stu-id="ee8f8-114">Requirement</span></span>          |    <span data-ttu-id="ee8f8-115">值</span><span class="sxs-lookup"><span data-stu-id="ee8f8-115">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8f8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee8f8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ee8f8-117">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="ee8f8-117">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

