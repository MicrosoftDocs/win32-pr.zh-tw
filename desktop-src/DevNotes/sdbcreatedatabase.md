---
description: 建立新的填充碼資料庫。
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936272"
---
# <a name="sdbcreatedatabase-function"></a><span data-ttu-id="06cb1-103">SdbCreateDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="06cb1-103">SdbCreateDatabase function</span></span>

<span data-ttu-id="06cb1-104">建立新的填充碼資料庫。</span><span class="sxs-lookup"><span data-stu-id="06cb1-104">Creates a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="06cb1-105">語法</span><span class="sxs-lookup"><span data-stu-id="06cb1-105">Syntax</span></span>


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="06cb1-106">參數</span><span class="sxs-lookup"><span data-stu-id="06cb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06cb1-107">*pwszPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06cb1-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cb1-108">應儲存資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="06cb1-108">The path where the database should be saved.</span></span> <span data-ttu-id="06cb1-109">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="06cb1-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="06cb1-110">*eType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06cb1-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cb1-111">路徑類型。</span><span class="sxs-lookup"><span data-stu-id="06cb1-111">The path type.</span></span> <span data-ttu-id="06cb1-112">如需值清單，請參閱 [**路徑 \_ 類型**](path-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="06cb1-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06cb1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="06cb1-113">Return value</span></span>

<span data-ttu-id="06cb1-114">函數會傳回填充碼資料庫的控制碼，或在失敗時傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="06cb1-114">The function returns a handle to the shim database or **NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="06cb1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="06cb1-115">Requirements</span></span>



| <span data-ttu-id="06cb1-116">需求</span><span class="sxs-lookup"><span data-stu-id="06cb1-116">Requirement</span></span> | <span data-ttu-id="06cb1-117">值</span><span class="sxs-lookup"><span data-stu-id="06cb1-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06cb1-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06cb1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06cb1-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06cb1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="06cb1-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06cb1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06cb1-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06cb1-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06cb1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="06cb1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06cb1-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06cb1-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06cb1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06cb1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06cb1-125">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="06cb1-125">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




