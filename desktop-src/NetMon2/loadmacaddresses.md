---
description: 監視器會呼叫 LoadMACAddresses 函式，以填入取自 HTML 設定字串變數之位址的 MAC 地址清單。
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: 'LoadMACAddresses 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511840"
---
# <a name="loadmacaddresses-function"></a><span data-ttu-id="0a185-103">LoadMACAddresses 函式</span><span class="sxs-lookup"><span data-stu-id="0a185-103">LoadMACAddresses function</span></span>

<span data-ttu-id="0a185-104">監視器會呼叫 **LoadMACAddresses** 函式，以填入取自 HTML 設定字串變數之位址的 MAC 地址清單。</span><span class="sxs-lookup"><span data-stu-id="0a185-104">The **LoadMACAddresses** function is called by the monitor to fill in a MAC address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a185-105">語法</span><span class="sxs-lookup"><span data-stu-id="0a185-105">Syntax</span></span>


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="0a185-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a185-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a185-107">*>-pconfig* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a185-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a185-108">[IMonitor：:D oconfigure](imonitor-doconfigure.md)方法傳遞給監視器的 HTML 設定字串指標。</span><span class="sxs-lookup"><span data-stu-id="0a185-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="0a185-109">*pVarName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a185-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a185-110">設定字串中變數名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="0a185-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="0a185-111">*ppAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0a185-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a185-112">指向位址陣列指標的指標。</span><span class="sxs-lookup"><span data-stu-id="0a185-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="0a185-113">如果找到在 *pVarName* 中指定的變數，而且其長度不是零，則此函式會使用 **HeapAllocMemory**) 配置足夠的空間 (，並將所有 MAC 位址儲存為數組。</span><span class="sxs-lookup"><span data-stu-id="0a185-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space (by using **HeapAllocMemory**) and stores all the MAC addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="0a185-114">*pNumAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0a185-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a185-115">**DWORD** 變數的指標，此變數會設定為取自設定字串的 MAC 位址數目。</span><span class="sxs-lookup"><span data-stu-id="0a185-115">Pointer to the **DWORD** variable that is set to the number of MAC addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a185-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a185-116">Return value</span></span>

<span data-ttu-id="0a185-117">如果函式成功， (找到變數名稱，且具有非零長度的字串，表示 MAC 位址) ，傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0a185-117">If the function is successful, (the variable name was found and had a non-zero-length string that represented MAC addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="0a185-118">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0a185-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a185-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a185-119">Requirements</span></span>



| <span data-ttu-id="0a185-120">需求</span><span class="sxs-lookup"><span data-stu-id="0a185-120">Requirement</span></span> | <span data-ttu-id="0a185-121">值</span><span class="sxs-lookup"><span data-stu-id="0a185-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0a185-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a185-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0a185-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a185-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0a185-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a185-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0a185-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a185-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0a185-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0a185-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a185-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="0a185-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0a185-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a185-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a185-129"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a185-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0a185-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0a185-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a185-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a185-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




