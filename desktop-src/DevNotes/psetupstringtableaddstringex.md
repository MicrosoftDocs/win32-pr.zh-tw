---
description: 將字串和額外的資料加入至資料表。
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: pSetupStringTableAddStringEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976013"
---
# <a name="psetupstringtableaddstringex-function"></a><span data-ttu-id="5b10d-103">pSetupStringTableAddStringEx 函式</span><span class="sxs-lookup"><span data-stu-id="5b10d-103">pSetupStringTableAddStringEx function</span></span>

<span data-ttu-id="5b10d-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="5b10d-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="5b10d-105">將字串和額外的資料加入至資料表。</span><span class="sxs-lookup"><span data-stu-id="5b10d-105">Adds a string and extra data to a table.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b10d-106">語法</span><span class="sxs-lookup"><span data-stu-id="5b10d-106">Syntax</span></span>


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a><span data-ttu-id="5b10d-107">參數</span><span class="sxs-lookup"><span data-stu-id="5b10d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b10d-108">*StringTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b10d-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b10d-109">字串資料表的指標。</span><span class="sxs-lookup"><span data-stu-id="5b10d-109">A pointer to the string table.</span></span>

</dd> <dt>

<span data-ttu-id="5b10d-110">*字串* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b10d-110">*String* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b10d-111">要加入至資料表的字串指標。</span><span class="sxs-lookup"><span data-stu-id="5b10d-111">A pointer to string to be added to the table.</span></span>

</dd> <dt>

<span data-ttu-id="5b10d-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5b10d-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b10d-113">此參數的值可以是 `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` 。</span><span class="sxs-lookup"><span data-stu-id="5b10d-113">The value of this parameter can be `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA`.</span></span>



| <span data-ttu-id="5b10d-114">值</span><span class="sxs-lookup"><span data-stu-id="5b10d-114">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="5b10d-115">意義</span><span class="sxs-lookup"><span data-stu-id="5b10d-115">Meaning</span></span>                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <span data-ttu-id="5b10d-116"><dt>**STRTAB \_區分 \_ 大小寫**</dt> <dt>0x001</dt></span><span class="sxs-lookup"><span data-stu-id="5b10d-116"><dt>**STRTAB\_CASE\_SENSITIVE**</dt> <dt>0x001</dt></span></span> </dl> | <span data-ttu-id="5b10d-117">字串會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5b10d-117">String is case sensitive.</span></span><br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <span data-ttu-id="5b10d-118"><dt>**STRTAB \_新增 \_ EXTRADATA**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="5b10d-118"><dt>**STRTAB\_NEW\_EXTRADATA**</dt> <dt>0x004</dt></span></span> </dl>    | <span data-ttu-id="5b10d-119">有額外的資料。</span><span class="sxs-lookup"><span data-stu-id="5b10d-119">There is extra data.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="5b10d-120">*ExtraData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5b10d-120">*ExtraData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b10d-121">額外資料物件的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="5b10d-121">A optional pointer to an extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="5b10d-122">*ExtraDataSize* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5b10d-122">*ExtraDataSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b10d-123">額外資料的大小。</span><span class="sxs-lookup"><span data-stu-id="5b10d-123">The size of the extra data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b10d-124">備註</span><span class="sxs-lookup"><span data-stu-id="5b10d-124">Remarks</span></span>

<span data-ttu-id="5b10d-125">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5b10d-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b10d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b10d-126">Requirements</span></span>



| <span data-ttu-id="5b10d-127">需求</span><span class="sxs-lookup"><span data-stu-id="5b10d-127">Requirement</span></span> | <span data-ttu-id="5b10d-128">值</span><span class="sxs-lookup"><span data-stu-id="5b10d-128">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b10d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5b10d-129">DLL</span></span><br/> | <dl> <span data-ttu-id="5b10d-130"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b10d-130"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
