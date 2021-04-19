---
description: 取得可用磁碟空間。
ms.assetid: 4b7f4938-9918-4625-b28d-faf22de56976
title: _GetDiskFreeSpaceEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetDiskFreeSpaceEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
ms.openlocfilehash: da4a8eefabf03f6330ac9c1f135482f27dd8aa18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991182"
---
# <a name="_getdiskfreespaceex-function"></a><span data-ttu-id="5f73e-103">\_GetDiskFreeSpaceEx 函式</span><span class="sxs-lookup"><span data-stu-id="5f73e-103">\_GetDiskFreeSpaceEx function</span></span>

<span data-ttu-id="5f73e-104">\[此函式是 **GetDiskFreeSpaceEx** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="5f73e-104">\[This function is a wrapper over the **GetDiskFreeSpaceEx** function.</span></span> <span data-ttu-id="5f73e-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5f73e-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="5f73e-106">應用程式應該直接呼叫 **GetDiskFreeSpaceEx** 。\]</span><span class="sxs-lookup"><span data-stu-id="5f73e-106">Applications should call **GetDiskFreeSpaceEx** directly.\]</span></span>

<span data-ttu-id="5f73e-107">取得可用磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="5f73e-107">Gets the free disk space.</span></span> <span data-ttu-id="5f73e-108">請參閱 [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa)。</span><span class="sxs-lookup"><span data-stu-id="5f73e-108">See [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f73e-109">語法</span><span class="sxs-lookup"><span data-stu-id="5f73e-109">Syntax</span></span>


```C++
BOOL _GetDiskFreeSpaceEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="5f73e-110">參數</span><span class="sxs-lookup"><span data-stu-id="5f73e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f73e-111">*...*</span><span class="sxs-lookup"><span data-stu-id="5f73e-111">*...*</span></span> 
<span data-ttu-id="5f73e-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5f73e-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5f73e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f73e-113">Requirements</span></span>



| <span data-ttu-id="5f73e-114">需求</span><span class="sxs-lookup"><span data-stu-id="5f73e-114">Requirement</span></span> | <span data-ttu-id="5f73e-115">值</span><span class="sxs-lookup"><span data-stu-id="5f73e-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f73e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5f73e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="5f73e-117"><dt>Msmdun80.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f73e-117"><dt>Msmdun80.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f73e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f73e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f73e-119">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="5f73e-119">**GetDiskFreeSpaceEx**</span></span>](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa)
</dt> </dl>

 

 
