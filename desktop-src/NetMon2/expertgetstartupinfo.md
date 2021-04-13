---
description: ExpertGetStartupInfo 函式會抓取專家的啟動設定資訊。
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: 'ExpertGetStartupInfo 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386102"
---
# <a name="expertgetstartupinfo-function"></a><span data-ttu-id="68518-103">ExpertGetStartupInfo 函式</span><span class="sxs-lookup"><span data-stu-id="68518-103">ExpertGetStartupInfo function</span></span>

<span data-ttu-id="68518-104">**ExpertGetStartupInfo** 函式會抓取專家的啟動設定資訊。</span><span class="sxs-lookup"><span data-stu-id="68518-104">The **ExpertGetStartupInfo** function retrieves the startup configuration information for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="68518-105">語法</span><span class="sxs-lookup"><span data-stu-id="68518-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="68518-106">參數</span><span class="sxs-lookup"><span data-stu-id="68518-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68518-107">*hExpertKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68518-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68518-108">獨特的專家識別碼。</span><span class="sxs-lookup"><span data-stu-id="68518-108">Unique expert identifier.</span></span> <span data-ttu-id="68518-109">網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。</span><span class="sxs-lookup"><span data-stu-id="68518-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="68518-110">*pExpertStartupInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="68518-110">*pExpertStartupInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68518-111">包含啟動資訊之 [EXPERTSTARTUPINFO](expertstartupinfo.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="68518-111">Pointer to an [EXPERTSTARTUPINFO](expertstartupinfo.md) structure that contains startup information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68518-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="68518-112">Return value</span></span>

<span data-ttu-id="68518-113">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="68518-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="68518-114">如果函式不成功，則傳回值為 NMERR。</span><span class="sxs-lookup"><span data-stu-id="68518-114">If the function is unsuccessful, the return value is NMERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="68518-115">備註</span><span class="sxs-lookup"><span data-stu-id="68518-115">Remarks</span></span>

<span data-ttu-id="68518-116">如果專家必須判斷所使用的啟動資訊，則會使用 **ExpertGetStartupInfo** 函數。</span><span class="sxs-lookup"><span data-stu-id="68518-116">The **ExpertGetStartupInfo** function is used if the expert must determine the startup information that is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="68518-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="68518-117">Requirements</span></span>



| <span data-ttu-id="68518-118">需求</span><span class="sxs-lookup"><span data-stu-id="68518-118">Requirement</span></span> | <span data-ttu-id="68518-119">值</span><span class="sxs-lookup"><span data-stu-id="68518-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="68518-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68518-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68518-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68518-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="68518-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68518-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68518-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68518-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="68518-124">標頭</span><span class="sxs-lookup"><span data-stu-id="68518-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="68518-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="68518-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="68518-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="68518-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="68518-127"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68518-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="68518-128">DLL</span><span class="sxs-lookup"><span data-stu-id="68518-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68518-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68518-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




