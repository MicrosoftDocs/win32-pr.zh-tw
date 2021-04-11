---
description: SelectNPPBlobFromTable 函式會從所提供的 NPP BLOB 資料表中選取一個 NIC。
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: 'SelectNPPBlobFromTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191502"
---
# <a name="selectnppblobfromtable-function"></a><span data-ttu-id="fe908-103">SelectNPPBlobFromTable 函式</span><span class="sxs-lookup"><span data-stu-id="fe908-103">SelectNPPBlobFromTable function</span></span>

<span data-ttu-id="fe908-104">**SelectNPPBlobFromTable** 函式會從所提供的 NPP BLOB 資料表中選取一個 NIC。</span><span class="sxs-lookup"><span data-stu-id="fe908-104">The **SelectNPPBlobFromTable** function selects a NIC from a supplied NPP BLOB table.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe908-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe908-105">Syntax</span></span>


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="fe908-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe908-107">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe908-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe908-108">顯示 [ **選取網路** ] 對話方塊之視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe908-108">Handle to the window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="fe908-109">*pBlobTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe908-109">*pBlobTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe908-110">提供的 BLOB 資料表指標。</span><span class="sxs-lookup"><span data-stu-id="fe908-110">Pointer to the supplied BLOB table.</span></span> <span data-ttu-id="fe908-111">網路監視器使用此資料表來填入 [ **選取網路** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fe908-111">Network Monitor uses this table to populate the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="fe908-112">*hBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe908-112">*hBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe908-113">代表所選 NIC 之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe908-113">Handle to the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe908-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe908-114">Return value</span></span>

<span data-ttu-id="fe908-115">如果函式成功且使用者選取 NIC，則傳回值為 NMERR \_ SUCCESS; *hBlob* 所指向的 BLOB 會填入。</span><span class="sxs-lookup"><span data-stu-id="fe908-115">If the function is successful and the user selects a NIC, the return value is NMERR\_SUCCESS; the BLOB pointed to by *hBlob* is filled in.</span></span>

<span data-ttu-id="fe908-116">如果使用者未選取 NIC，則傳回值為 NMERR \_ NO \_ NPP \_ SELECTED。</span><span class="sxs-lookup"><span data-stu-id="fe908-116">If the user does not select a NIC, the return value is NMERR\_NO\_NPP\_SELECTED.</span></span>

<span data-ttu-id="fe908-117">如果函式不成功，則傳回值為另一個 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="fe908-117">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe908-118">備註</span><span class="sxs-lookup"><span data-stu-id="fe908-118">Remarks</span></span>

<span data-ttu-id="fe908-119">當呼叫時，網路監視器會顯示 [ **選取網路** ] 對話方塊，您可以使用此對話方塊來選取 NIC。</span><span class="sxs-lookup"><span data-stu-id="fe908-119">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="fe908-120">代表所選 NIC 的 NPP BLOB 會傳回到呼叫應用程式。</span><span class="sxs-lookup"><span data-stu-id="fe908-120">The NPP BLOB that represents the selected NIC returns to the calling application.</span></span>

<span data-ttu-id="fe908-121">若要瞭解您可以選取 Nic 的各種方式，請參閱 [選取網路介面卡](selecting-a-network-interface-card.md)</span><span class="sxs-lookup"><span data-stu-id="fe908-121">To learn the various ways you can select NICs, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="fe908-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe908-122">Requirements</span></span>



| <span data-ttu-id="fe908-123">需求</span><span class="sxs-lookup"><span data-stu-id="fe908-123">Requirement</span></span> | <span data-ttu-id="fe908-124">值</span><span class="sxs-lookup"><span data-stu-id="fe908-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe908-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe908-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fe908-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe908-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fe908-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe908-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fe908-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe908-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fe908-129">標頭</span><span class="sxs-lookup"><span data-stu-id="fe908-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe908-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="fe908-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="fe908-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe908-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe908-132"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe908-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe908-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fe908-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe908-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe908-134"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe908-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe908-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe908-136">GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="fe908-136">GetNPPBlobFromUI</span></span>](getnppblobfromui.md)
</dt> <dt>

[<span data-ttu-id="fe908-137">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="fe908-137">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="fe908-138">特殊 BLOB 專案</span><span class="sxs-lookup"><span data-stu-id="fe908-138">Special BLOB Entries</span></span>](special-blob-entries.md)
</dt> </dl>

 

 




