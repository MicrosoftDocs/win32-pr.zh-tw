---
description: 監視器會呼叫 LoadIPAddresses 函式，以填入取自 HTML 設定字串變數之位址的 IP 位址清單。
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: 'LoadIPAddresses 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998925"
---
# <a name="loadipaddresses-function"></a><span data-ttu-id="892cd-103">LoadIPAddresses 函式</span><span class="sxs-lookup"><span data-stu-id="892cd-103">LoadIPAddresses function</span></span>

<span data-ttu-id="892cd-104">監視器會呼叫 **LoadIPAddresses** 函式，以填入取自 HTML 設定字串變數之位址的 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="892cd-104">The **LoadIPAddresses** function is called by the monitor to fill in an IP address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="892cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="892cd-105">Syntax</span></span>


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="892cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="892cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="892cd-107">*>-pconfig* \[在\]</span><span class="sxs-lookup"><span data-stu-id="892cd-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="892cd-108">[IMonitor：:D oconfigure](imonitor-doconfigure.md)方法傳遞給監視器的 HTML 設定字串指標。</span><span class="sxs-lookup"><span data-stu-id="892cd-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="892cd-109">*pVarName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="892cd-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="892cd-110">設定字串中變數名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="892cd-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="892cd-111">*ppAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="892cd-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="892cd-112">指向位址陣列指標的指標。</span><span class="sxs-lookup"><span data-stu-id="892cd-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="892cd-113">如果找到在 *pVarName* 中指定的變數，而且其長度為非零，則此函式會配置足夠的空間，並將所有 IP 位址儲存為數組。</span><span class="sxs-lookup"><span data-stu-id="892cd-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space and stores all the IP addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="892cd-114">*pNumAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="892cd-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="892cd-115">**DWORD** 變數的指標，此變數會設定為取自設定字串的 IP 位址數目。</span><span class="sxs-lookup"><span data-stu-id="892cd-115">Pointer to the **DWORD** variable that is set to the number of IP addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="892cd-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="892cd-116">Return value</span></span>

<span data-ttu-id="892cd-117">如果函式成功 (已找到變數名稱，且具有表示 IP 位址) 的非零長度字串，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="892cd-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IP addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="892cd-118">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="892cd-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="892cd-119">備註</span><span class="sxs-lookup"><span data-stu-id="892cd-119">Remarks</span></span>

<span data-ttu-id="892cd-120">IP 位址必須是 x.x 格式 (例如，127.0.0.1) ）。</span><span class="sxs-lookup"><span data-stu-id="892cd-120">The IP addresses must be in x.x.x.x format (for example, 127.0.0.1).</span></span>

## <a name="requirements"></a><span data-ttu-id="892cd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="892cd-121">Requirements</span></span>



| <span data-ttu-id="892cd-122">需求</span><span class="sxs-lookup"><span data-stu-id="892cd-122">Requirement</span></span> | <span data-ttu-id="892cd-123">值</span><span class="sxs-lookup"><span data-stu-id="892cd-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="892cd-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="892cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="892cd-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="892cd-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="892cd-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="892cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="892cd-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="892cd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="892cd-128">標頭</span><span class="sxs-lookup"><span data-stu-id="892cd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="892cd-129"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="892cd-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="892cd-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="892cd-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="892cd-131"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="892cd-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="892cd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="892cd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="892cd-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="892cd-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




