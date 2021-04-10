---
description: IsRemoteNPP 函數會指出指定的 BLOB 是否指定遠端 NPP。
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: 'IsRemoteNPP 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692372"
---
# <a name="isremotenpp-function"></a><span data-ttu-id="896bf-103">IsRemoteNPP 函式</span><span class="sxs-lookup"><span data-stu-id="896bf-103">IsRemoteNPP function</span></span>

<span data-ttu-id="896bf-104">**IsRemoteNPP** 函數會指出指定的 BLOB 是否指定遠端 NPP。</span><span class="sxs-lookup"><span data-stu-id="896bf-104">The **IsRemoteNPP** function indicates whether the given BLOB specifies a remote NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="896bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="896bf-105">Syntax</span></span>


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="896bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="896bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="896bf-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="896bf-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="896bf-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="896bf-108">Handle to a BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="896bf-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="896bf-109">Return value</span></span>

<span data-ttu-id="896bf-110">如果函式成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="896bf-110">If the function is successful, the return value is **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="896bf-111">備註</span><span class="sxs-lookup"><span data-stu-id="896bf-111">Remarks</span></span>

<span data-ttu-id="896bf-112">您可以使用此函式來測試遠端類別是否存在。</span><span class="sxs-lookup"><span data-stu-id="896bf-112">Use this function to test whether a remote category exists.</span></span>

<span data-ttu-id="896bf-113">確定遠端和本機電腦名稱稱不同。</span><span class="sxs-lookup"><span data-stu-id="896bf-113">Make certain that the remote and local computer names are different.</span></span>

## <a name="requirements"></a><span data-ttu-id="896bf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="896bf-114">Requirements</span></span>



| <span data-ttu-id="896bf-115">需求</span><span class="sxs-lookup"><span data-stu-id="896bf-115">Requirement</span></span> | <span data-ttu-id="896bf-116">值</span><span class="sxs-lookup"><span data-stu-id="896bf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="896bf-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="896bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="896bf-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="896bf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="896bf-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="896bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="896bf-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="896bf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="896bf-121">標頭</span><span class="sxs-lookup"><span data-stu-id="896bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="896bf-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="896bf-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="896bf-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="896bf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="896bf-124"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="896bf-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="896bf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="896bf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="896bf-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="896bf-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




