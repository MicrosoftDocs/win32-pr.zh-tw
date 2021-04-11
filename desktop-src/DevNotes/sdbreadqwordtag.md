---
Description: 抓取指定之 TAGID 的 QWORD 值。
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: SdbReadQWORDTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385198"
---
# <a name="sdbreadqwordtag-function"></a><span data-ttu-id="a93a1-103">SdbReadQWORDTag 函式</span><span class="sxs-lookup"><span data-stu-id="a93a1-103">SdbReadQWORDTag function</span></span>

<span data-ttu-id="a93a1-104">抓取指定之 **TAGID** 的 **QWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="a93a1-104">Retrieves the **QWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="a93a1-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="a93a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="a93a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a93a1-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a93a1-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a93a1-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a93a1-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="a93a1-109">*tiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a93a1-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a93a1-110">對應至要抓取之資料的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="a93a1-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a93a1-111">*qwDefault* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a93a1-111">*qwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a93a1-112">失敗時要傳回的預設值。</span><span class="sxs-lookup"><span data-stu-id="a93a1-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a93a1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a93a1-113">Return value</span></span>

<span data-ttu-id="a93a1-114">函數會在失敗時傳回成功或 *qwDefault* 的值。</span><span class="sxs-lookup"><span data-stu-id="a93a1-114">The function returns the value on success or *qwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a93a1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a93a1-115">Requirements</span></span>



| <span data-ttu-id="a93a1-116">需求</span><span class="sxs-lookup"><span data-stu-id="a93a1-116">Requirement</span></span> | <span data-ttu-id="a93a1-117">值</span><span class="sxs-lookup"><span data-stu-id="a93a1-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a93a1-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a93a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a93a1-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a93a1-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a93a1-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a93a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a93a1-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a93a1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a93a1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a93a1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a93a1-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a93a1-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a93a1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a93a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93a1-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="a93a1-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="a93a1-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="a93a1-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="a93a1-127">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="a93a1-127">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="a93a1-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="a93a1-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




