---
description: 監視器會呼叫 LoadDWORD 函式，以使用取自 HTML 設定字串變數的值來設定 DWORD 變數。
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: 'LoadDWORD 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979419"
---
# <a name="loaddword-function"></a><span data-ttu-id="e7d85-103">LoadDWORD 函式</span><span class="sxs-lookup"><span data-stu-id="e7d85-103">LoadDWORD function</span></span>

<span data-ttu-id="e7d85-104">監視器會呼叫 **LoadDWORD** 函式，以使用取自 HTML 設定字串變數的值來設定 **DWORD** 變數。</span><span class="sxs-lookup"><span data-stu-id="e7d85-104">The **LoadDWORD** function is called by the monitor to set a **DWORD** variable with a value taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d85-105">語法</span><span class="sxs-lookup"><span data-stu-id="e7d85-105">Syntax</span></span>


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e7d85-106">參數</span><span class="sxs-lookup"><span data-stu-id="e7d85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d85-107">*>-pconfig* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7d85-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d85-108">[IMonitor：:D oconfigure](imonitor-doconfigure.md)方法傳遞給監視器的 HTML 設定字串指標。</span><span class="sxs-lookup"><span data-stu-id="e7d85-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e7d85-109">*pVarName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7d85-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d85-110">設定字串中變數名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="e7d85-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="e7d85-111">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7d85-111">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d85-112">**DWORD** 變數的指標，此變數會設定為設定字串變數的值。</span><span class="sxs-lookup"><span data-stu-id="e7d85-112">Pointer to the **DWORD** variable that is set to the value of the configuration string variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d85-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7d85-113">Return value</span></span>

<span data-ttu-id="e7d85-114">如果函式成功 (如果找到變數名稱，且) 長度為非零長度的字串，則會插入 **DWORD** ，且傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="e7d85-114">If the function is successful (if the variable name was found and had a non-zero-length string), the **DWORD** is inserted, and the return value is **TRUE**.</span></span>

<span data-ttu-id="e7d85-115">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e7d85-115">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d85-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7d85-116">Requirements</span></span>



| <span data-ttu-id="e7d85-117">需求</span><span class="sxs-lookup"><span data-stu-id="e7d85-117">Requirement</span></span> | <span data-ttu-id="e7d85-118">值</span><span class="sxs-lookup"><span data-stu-id="e7d85-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d85-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7d85-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d85-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7d85-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e7d85-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7d85-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d85-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7d85-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e7d85-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e7d85-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7d85-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e7d85-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e7d85-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7d85-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7d85-126"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7d85-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e7d85-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e7d85-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7d85-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7d85-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




