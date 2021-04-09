---
description: 關閉指定的資料庫。
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: SdbCloseDatabaseWrite 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847224"
---
# <a name="sdbclosedatabasewrite-function"></a><span data-ttu-id="511ab-103">SdbCloseDatabaseWrite 函式</span><span class="sxs-lookup"><span data-stu-id="511ab-103">SdbCloseDatabaseWrite function</span></span>

<span data-ttu-id="511ab-104">關閉指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="511ab-104">Closes the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="511ab-105">語法</span><span class="sxs-lookup"><span data-stu-id="511ab-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="511ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="511ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="511ab-107">*pdb* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="511ab-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="511ab-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="511ab-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="511ab-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="511ab-109">Return value</span></span>

<span data-ttu-id="511ab-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="511ab-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="511ab-111">備註</span><span class="sxs-lookup"><span data-stu-id="511ab-111">Remarks</span></span>

<span data-ttu-id="511ab-112">此函數會呼叫 [**SdbCloseDatabase**](sdbclosedatabase.md);因此，這兩個函數是相等的。</span><span class="sxs-lookup"><span data-stu-id="511ab-112">This function calls [**SdbCloseDatabase**](sdbclosedatabase.md); therefore, these two functions are equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="511ab-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="511ab-113">Requirements</span></span>



| <span data-ttu-id="511ab-114">需求</span><span class="sxs-lookup"><span data-stu-id="511ab-114">Requirement</span></span> | <span data-ttu-id="511ab-115">值</span><span class="sxs-lookup"><span data-stu-id="511ab-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="511ab-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="511ab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="511ab-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="511ab-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="511ab-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="511ab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="511ab-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="511ab-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="511ab-120">DLL</span><span class="sxs-lookup"><span data-stu-id="511ab-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="511ab-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="511ab-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="511ab-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="511ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511ab-123">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="511ab-123">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="511ab-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="511ab-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="511ab-125">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="511ab-125">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> </dl>

 

 




