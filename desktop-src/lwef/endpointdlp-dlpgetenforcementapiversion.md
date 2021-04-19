---
description: 在目前的裝置上，抓取端點資料遺失防止 (DLP) API 的版本。
title: 'DlpGetEnforcementApiVersion 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495536"
---
# <a name="dlpgetenforcementapiversion-function"></a><span data-ttu-id="36884-103">DlpGetEnforcementApiVersion 函式</span><span class="sxs-lookup"><span data-stu-id="36884-103">DlpGetEnforcementApiVersion function</span></span>

<span data-ttu-id="36884-104">在目前的裝置上，抓取端點資料遺失防止 (DLP) API 的版本。</span><span class="sxs-lookup"><span data-stu-id="36884-104">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>

## <a name="syntax"></a><span data-ttu-id="36884-105">語法</span><span class="sxs-lookup"><span data-stu-id="36884-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a><span data-ttu-id="36884-106">參數</span><span class="sxs-lookup"><span data-stu-id="36884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36884-107">*MajorVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36884-107">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36884-108">指定主要版本號碼的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="36884-108">A **DWORD** specifying the major version number.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="36884-109">*MajorVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36884-109">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36884-110">指定次要版本號碼的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="36884-110">A **DWORD** specifying the minor version number.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="36884-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="36884-111">Return value</span></span>

<span data-ttu-id="36884-112">傳回 HRESULT （包括但不限於下列值）。</span><span class="sxs-lookup"><span data-stu-id="36884-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="36884-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="36884-113">HRESULT</span></span> | <span data-ttu-id="36884-114">描述</span><span class="sxs-lookup"><span data-stu-id="36884-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="36884-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="36884-115">S_OK</span></span> | <span data-ttu-id="36884-116">函數已順利完成</span><span class="sxs-lookup"><span data-stu-id="36884-116">The function completed successfully</span></span> |




## <a name="remarks"></a><span data-ttu-id="36884-117">備註</span><span class="sxs-lookup"><span data-stu-id="36884-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="36884-118">需求</span><span class="sxs-lookup"><span data-stu-id="36884-118">Requirements</span></span>



| <span data-ttu-id="36884-119">需求</span><span class="sxs-lookup"><span data-stu-id="36884-119">Requirement</span></span>          |    <span data-ttu-id="36884-120">值</span><span class="sxs-lookup"><span data-stu-id="36884-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36884-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36884-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36884-122">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="36884-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="36884-123">DLL</span><span class="sxs-lookup"><span data-stu-id="36884-123">DLL</span></span><br/>                      | <span data-ttu-id="36884-124">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="36884-124">EndpointDlp.dll</span></span> |