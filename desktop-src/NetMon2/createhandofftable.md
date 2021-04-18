---
description: CreateHandoffTable 函式會建立一個包含在剖析器 INI 檔案中儲存之遞交集資訊的遞交資料表。
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: 'CreateHandoffTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983480"
---
# <a name="createhandofftable-function"></a><span data-ttu-id="2a3e0-103">CreateHandoffTable 函式</span><span class="sxs-lookup"><span data-stu-id="2a3e0-103">CreateHandoffTable function</span></span>

<span data-ttu-id="2a3e0-104">**CreateHandoffTable** 函式會建立一個包含在剖析器 INI 檔案中儲存之遞交集資訊的 [*遞交資料表*](h.md)。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-104">The **CreateHandoffTable** function creates a [*handoff table*](h.md) that includes the handoff set information stored in the INI file of the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a3e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="2a3e0-105">Syntax</span></span>


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a><span data-ttu-id="2a3e0-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a3e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a3e0-107">*secName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a3e0-107">*secName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a3e0-108">字串，表示要在其中放置遞交集資訊的 INI 檔區段。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-108">String that indicates the section of the INI file where the handoff set information is located.</span></span>

</dd> <dt>

<span data-ttu-id="2a3e0-109">*iniFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a3e0-109">*iniFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a3e0-110">包含剖析器 INI 檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-110">String that includes the name of the parser INI file.</span></span>

</dd> <dt>

<span data-ttu-id="2a3e0-111">*hTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2a3e0-111">*hTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a3e0-112">網路監視器所建立和維護的 **HANDOFFTABLE** 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-112">Handle to a **HANDOFFTABLE** structure created and maintained by Network Monitor.</span></span>

</dd> <dt>

<span data-ttu-id="2a3e0-113">*nMaxProtocolEntries* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a3e0-113">*nMaxProtocolEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a3e0-114">指定交付資料表可處理的專案數上限的數位。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-114">Number that specifies the maximum number of entries that the handoff table can process.</span></span>

</dd> <dt>

<span data-ttu-id="2a3e0-115">*基底* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a3e0-115">*base* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a3e0-116">儲存在 INI 檔案中的交付集數位的數位基底。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-116">Numerical base of handoff set numbers stored in the INI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a3e0-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a3e0-117">Return value</span></span>

<span data-ttu-id="2a3e0-118">如果函式成功，則傳回值是提交資料表中的專案數。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-118">If the function is successful, the return value is the number of entries in the handoff table.</span></span>

<span data-ttu-id="2a3e0-119">如果函式不成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-119">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a3e0-120">備註</span><span class="sxs-lookup"><span data-stu-id="2a3e0-120">Remarks</span></span>

<span data-ttu-id="2a3e0-121">網路監視器所建立的交付資料表是以剖析器 INI 中提供的資訊為基礎。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-121">The handoff table created by Network Monitor is based on information provided in the parser INI.</span></span> <span data-ttu-id="2a3e0-122">然後，您可以使用提交資料表的傳回控制碼，來取得包含在資料表中其中一個通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-122">The returned handle to the handoff table can then be used to obtain a handle to one of the protocols included in the table.</span></span> <span data-ttu-id="2a3e0-123">若要取得其中一個通訊協定的控制碼，請呼叫 [GetProtocolFromTable](getprotocolfromtable.md)。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-123">To obtain a handle of one of these protocols, call [GetProtocolFromTable](getprotocolfromtable.md).</span></span>

<span data-ttu-id="2a3e0-124">請注意，剖析器應用程式永遠不會直接存取 **HANDOFFTABLE** 結構。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-124">Notice that the parser application never accesses the **HANDOFFTABLE** structure directly.</span></span> <span data-ttu-id="2a3e0-125">此結構是由網路監視器建立和維護。</span><span class="sxs-lookup"><span data-stu-id="2a3e0-125">This structure is created and maintained by Network Monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3e0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a3e0-126">Requirements</span></span>



| <span data-ttu-id="2a3e0-127">需求</span><span class="sxs-lookup"><span data-stu-id="2a3e0-127">Requirement</span></span> | <span data-ttu-id="2a3e0-128">值</span><span class="sxs-lookup"><span data-stu-id="2a3e0-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3e0-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a3e0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3e0-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a3e0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2a3e0-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a3e0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3e0-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a3e0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2a3e0-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2a3e0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a3e0-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2a3e0-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2a3e0-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a3e0-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a3e0-136"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a3e0-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2a3e0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2a3e0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a3e0-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a3e0-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a3e0-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a3e0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a3e0-140">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="2a3e0-140">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> <dt>

[<span data-ttu-id="2a3e0-141">HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="2a3e0-141">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




