---
description: 建立或開啟檔案。
ms.assetid: 2a993f45-7f87-4b9e-bccc-277477558d3c
title: _CreateFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _CreateFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: becd7fed9e32385409b78e00169191a12b550e3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000750"
---
# <a name="_createfile-function"></a><span data-ttu-id="19a58-103">\_CreateFile 函式</span><span class="sxs-lookup"><span data-stu-id="19a58-103">\_CreateFile function</span></span>

<span data-ttu-id="19a58-104">\[此函式是 **CreateFile** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="19a58-104">\[This function is a wrapper over the **CreateFile** function.</span></span> <span data-ttu-id="19a58-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="19a58-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="19a58-106">應用程式應該直接呼叫 **CreateFile** 。\]</span><span class="sxs-lookup"><span data-stu-id="19a58-106">Applications should call **CreateFile** directly.\]</span></span>

<span data-ttu-id="19a58-107">建立或開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="19a58-107">Creates or opens a file.</span></span> <span data-ttu-id="19a58-108">請參閱 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)。</span><span class="sxs-lookup"><span data-stu-id="19a58-108">See [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span></span>

## <a name="syntax"></a><span data-ttu-id="19a58-109">語法</span><span class="sxs-lookup"><span data-stu-id="19a58-109">Syntax</span></span>


```C++
BOOL _CreateFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="19a58-110">參數</span><span class="sxs-lookup"><span data-stu-id="19a58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a58-111">*...*</span><span class="sxs-lookup"><span data-stu-id="19a58-111">*...*</span></span> 
<span data-ttu-id="19a58-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="19a58-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="19a58-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="19a58-113">Requirements</span></span>



| <span data-ttu-id="19a58-114">需求</span><span class="sxs-lookup"><span data-stu-id="19a58-114">Requirement</span></span> | <span data-ttu-id="19a58-115">值</span><span class="sxs-lookup"><span data-stu-id="19a58-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a58-116">DLL</span><span class="sxs-lookup"><span data-stu-id="19a58-116">DLL</span></span><br/> | <dl> <span data-ttu-id="19a58-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19a58-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a58-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19a58-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a58-119">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="19a58-119">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> </dl>

 

