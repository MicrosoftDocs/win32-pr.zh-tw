---
title: 'FreeSoHAttributeValue 函式 (NapUtil) '
description: 釋放 SoHAttributeValue 資料結構。
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- FreeSoHAttributeValue 函數 NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025424"
---
# <a name="freesohattributevalue-function"></a><span data-ttu-id="fc12c-104">FreeSoHAttributeValue 函式</span><span class="sxs-lookup"><span data-stu-id="fc12c-104">FreeSoHAttributeValue function</span></span>

> [!Note]  
> <span data-ttu-id="fc12c-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="fc12c-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fc12c-106">**FreeSoHAttributeValue** 函式會釋出 [**SoHAttributeValue**](sohattributevalue-union.md)的資料結構。</span><span class="sxs-lookup"><span data-stu-id="fc12c-106">The **FreeSoHAttributeValue** function frees an [**SoHAttributeValue**](sohattributevalue-union.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc12c-107">語法</span><span class="sxs-lookup"><span data-stu-id="fc12c-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="fc12c-108">參數</span><span class="sxs-lookup"><span data-stu-id="fc12c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc12c-109">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc12c-109">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12c-110">[**SoHAttributeType**](sohattributetype-enum.md)值，指定要釋放的 SoH 屬性值類型。</span><span class="sxs-lookup"><span data-stu-id="fc12c-110">A [**SoHAttributeType**](sohattributetype-enum.md) value that specifies the type of SoH attribute value to free.</span></span>

</dd> <dt>

<span data-ttu-id="fc12c-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc12c-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12c-112">要釋放的 [**SoHAttributeValue**](sohattributevalue-union.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="fc12c-112">A pointer to the [**SoHAttributeValue**](sohattributevalue-union.md) to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc12c-113">備註</span><span class="sxs-lookup"><span data-stu-id="fc12c-113">Remarks</span></span>

<span data-ttu-id="fc12c-114">NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：</span><span class="sxs-lookup"><span data-stu-id="fc12c-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="fc12c-115">呼叫端會配置和釋放 **In** 參數。</span><span class="sxs-lookup"><span data-stu-id="fc12c-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="fc12c-116">**Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。</span><span class="sxs-lookup"><span data-stu-id="fc12c-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="fc12c-117">**In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。</span><span class="sxs-lookup"><span data-stu-id="fc12c-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="fc12c-118">釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="fc12c-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc12c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc12c-119">Requirements</span></span>



| <span data-ttu-id="fc12c-120">需求</span><span class="sxs-lookup"><span data-stu-id="fc12c-120">Requirement</span></span> | <span data-ttu-id="fc12c-121">值</span><span class="sxs-lookup"><span data-stu-id="fc12c-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc12c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc12c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fc12c-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc12c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fc12c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc12c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fc12c-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc12c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fc12c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="fc12c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc12c-127"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc12c-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="fc12c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fc12c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc12c-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc12c-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





