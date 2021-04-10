---
description: LoadIPXAddresses 函式會由監視器呼叫，以填入取自 HTML 設定字串變數的 IPX 地址清單。
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: 'LoadIPXAddresses 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194542"
---
# <a name="loadipxaddresses-function"></a><span data-ttu-id="d11e2-103">LoadIPXAddresses 函式</span><span class="sxs-lookup"><span data-stu-id="d11e2-103">LoadIPXAddresses function</span></span>

<span data-ttu-id="d11e2-104">**LoadIPXAddresses** 函式會由監視器呼叫，以填入取自 HTML 設定字串變數的 IPX 地址清單。</span><span class="sxs-lookup"><span data-stu-id="d11e2-104">The **LoadIPXAddresses** function is called by the monitor to fill in an IPX address list taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="d11e2-105">Syntax</span></span>


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="d11e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="d11e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d11e2-107">*>-pconfig* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d11e2-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d11e2-108">[IMonitor：:D oconfigure](imonitor-doconfigure.md)方法傳遞給監視器的 HTML 設定字串指標。</span><span class="sxs-lookup"><span data-stu-id="d11e2-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="d11e2-109">*pVarName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d11e2-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d11e2-110">設定字串中變數名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="d11e2-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="d11e2-111">*ppAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d11e2-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d11e2-112">指向位址陣列指標的指標。</span><span class="sxs-lookup"><span data-stu-id="d11e2-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="d11e2-113">如果找到在 *pVarName* 中指定的變數，且具有非零長度的，則會使用 **HeapAllocMemory**) 來配置 (的足夠空間，而且所有的 IPX 位址都會儲存為數組。</span><span class="sxs-lookup"><span data-stu-id="d11e2-113">If the variable specified in *pVarName* is found and has a non-zero-length, sufficient space is allocated (by using **HeapAllocMemory**), and all the IPX addresses are stored as an array.</span></span>

</dd> <dt>

<span data-ttu-id="d11e2-114">*pNumAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d11e2-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d11e2-115">**DWORD** 變數的指標，此變數會設定為取自設定字串的 IPX 位址數目。</span><span class="sxs-lookup"><span data-stu-id="d11e2-115">Pointer to the **DWORD** variable that is set to the number of IPX addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d11e2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d11e2-116">Return value</span></span>

<span data-ttu-id="d11e2-117">如果函式成功 (已找到變數名稱，且有非零長度的字串表示) 的 IPX 位址，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d11e2-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IPX addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="d11e2-118">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d11e2-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d11e2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d11e2-119">Requirements</span></span>



| <span data-ttu-id="d11e2-120">需求</span><span class="sxs-lookup"><span data-stu-id="d11e2-120">Requirement</span></span> | <span data-ttu-id="d11e2-121">值</span><span class="sxs-lookup"><span data-stu-id="d11e2-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d11e2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d11e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d11e2-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d11e2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d11e2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d11e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d11e2-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d11e2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d11e2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d11e2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d11e2-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="d11e2-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d11e2-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d11e2-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d11e2-129"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d11e2-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d11e2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d11e2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d11e2-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d11e2-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




