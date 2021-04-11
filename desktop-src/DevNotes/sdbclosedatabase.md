---
description: 關閉指定的填充碼資料庫。
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: SdbCloseDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025909"
---
# <a name="sdbclosedatabase-function"></a><span data-ttu-id="a2341-103">SdbCloseDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="a2341-103">SdbCloseDatabase function</span></span>

<span data-ttu-id="a2341-104">關閉指定的填充碼資料庫。</span><span class="sxs-lookup"><span data-stu-id="a2341-104">Closes the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2341-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2341-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="a2341-106">參數</span><span class="sxs-lookup"><span data-stu-id="a2341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2341-107">*pdb* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a2341-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2341-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a2341-108">A handle to the shim database.</span></span> <span data-ttu-id="a2341-109">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a2341-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2341-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2341-110">Return value</span></span>

<span data-ttu-id="a2341-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a2341-111">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2341-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2341-112">Requirements</span></span>



| <span data-ttu-id="a2341-113">需求</span><span class="sxs-lookup"><span data-stu-id="a2341-113">Requirement</span></span> | <span data-ttu-id="a2341-114">值</span><span class="sxs-lookup"><span data-stu-id="a2341-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2341-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2341-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a2341-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2341-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a2341-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2341-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a2341-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2341-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a2341-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a2341-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2341-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2341-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2341-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2341-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2341-122">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="a2341-122">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




