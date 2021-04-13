---
description: 關閉使用 SdbInitDatabase 函數初始化的填充碼資料庫。
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: SdbReleaseDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510495"
---
# <a name="sdbreleasedatabase-function"></a><span data-ttu-id="b5d95-103">SdbReleaseDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="b5d95-103">SdbReleaseDatabase function</span></span>

<span data-ttu-id="b5d95-104">關閉使用 [**SdbInitDatabase**](sdbinitdatabase.md) 函數初始化的填充碼資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5d95-104">Closes the shim database initialized using the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d95-105">語法</span><span class="sxs-lookup"><span data-stu-id="b5d95-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a><span data-ttu-id="b5d95-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5d95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d95-107">*hSDB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5d95-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d95-108">[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b5d95-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d95-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5d95-109">Return value</span></span>

<span data-ttu-id="b5d95-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b5d95-110">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d95-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5d95-111">Requirements</span></span>



| <span data-ttu-id="b5d95-112">需求</span><span class="sxs-lookup"><span data-stu-id="b5d95-112">Requirement</span></span> | <span data-ttu-id="b5d95-113">值</span><span class="sxs-lookup"><span data-stu-id="b5d95-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d95-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5d95-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d95-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5d95-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b5d95-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5d95-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d95-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5d95-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b5d95-118">DLL</span><span class="sxs-lookup"><span data-stu-id="b5d95-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5d95-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5d95-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d95-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5d95-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d95-121">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="b5d95-121">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




