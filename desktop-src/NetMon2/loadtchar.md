---
description: 監視器會呼叫 LoadTCHAR 函式，將字串變數設定為取自 HTML 設定字串的字串。
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: 'LoadTCHAR 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972065"
---
# <a name="loadtchar-function"></a><span data-ttu-id="a7719-103">LoadTCHAR 函式</span><span class="sxs-lookup"><span data-stu-id="a7719-103">LoadTCHAR function</span></span>

<span data-ttu-id="a7719-104">監視器會呼叫 **LoadTCHAR** 函式，將字串變數設定為取自 HTML 設定字串的字串。</span><span class="sxs-lookup"><span data-stu-id="a7719-104">The **LoadTCHAR** function is called by monitors to set a string variable to a string taken from an HTML configuration string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7719-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7719-105">Syntax</span></span>


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a><span data-ttu-id="a7719-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7719-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7719-107">*>-pconfig* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7719-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7719-108">[IMonitor：:D oconfigure](imonitor-doconfigure.md)方法傳遞給監視器的 HTML 設定字串指標。</span><span class="sxs-lookup"><span data-stu-id="a7719-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="a7719-109">*pVarName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7719-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7719-110">設定字串中變數名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="a7719-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="a7719-111">*ppszString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a7719-111">*ppszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7719-112">字串指標的指標。</span><span class="sxs-lookup"><span data-stu-id="a7719-112">Pointer to a string pointer.</span></span> <span data-ttu-id="a7719-113">如果找到要求的變數名稱，則會配置字串並將其指派給這個指標。</span><span class="sxs-lookup"><span data-stu-id="a7719-113">If the requested variable name is found, the string is allocated and assigned to this pointer.</span></span> <span data-ttu-id="a7719-114">使用者會以負責任的方式釋放與字串相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a7719-114">It is the user's responsibly to free the memory associated with the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7719-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7719-115">Return value</span></span>

<span data-ttu-id="a7719-116">如果函式成功 (如果找到變數名稱，且) 長度為非零長度的字串，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a7719-116">If the function is successful (if the variable name was found and had a non-zero-length string), the return value is **TRUE**.</span></span>

<span data-ttu-id="a7719-117">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a7719-117">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7719-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7719-118">Requirements</span></span>



| <span data-ttu-id="a7719-119">需求</span><span class="sxs-lookup"><span data-stu-id="a7719-119">Requirement</span></span> | <span data-ttu-id="a7719-120">值</span><span class="sxs-lookup"><span data-stu-id="a7719-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7719-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7719-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a7719-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7719-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a7719-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7719-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a7719-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7719-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a7719-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a7719-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7719-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a7719-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a7719-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="a7719-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7719-128"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7719-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a7719-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a7719-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7719-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7719-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




