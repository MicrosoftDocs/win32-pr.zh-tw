---
description: 選取註冊 NIC。
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: 'GetNPPBlobFromUI 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944519"
---
# <a name="getnppblobfromui-function"></a><span data-ttu-id="f5a16-103">GetNPPBlobFromUI 函式</span><span class="sxs-lookup"><span data-stu-id="f5a16-103">GetNPPBlobFromUI function</span></span>

<span data-ttu-id="f5a16-104">**GetNPPBlobFromUI** 函式會選取註冊 NIC。</span><span class="sxs-lookup"><span data-stu-id="f5a16-104">The **GetNPPBlobFromUI** function selects a register NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a16-105">語法</span><span class="sxs-lookup"><span data-stu-id="f5a16-105">Syntax</span></span>


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="f5a16-106">參數</span><span class="sxs-lookup"><span data-stu-id="f5a16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a16-107">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5a16-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a16-108">顯示 [ **選取網路** ] 對話方塊之視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f5a16-108">A handle to a window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f5a16-109">*hFilterBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5a16-109">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a16-110">[*篩選 BLOB*](f.md)的控制碼，用來限制顯示的 nic。</span><span class="sxs-lookup"><span data-stu-id="f5a16-110">A handle to a [*filter BLOB*](f.md) used to limit which NICs are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="f5a16-111">*phBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f5a16-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a16-112">BLOB 控制碼的指標，代表選取的 NIC。</span><span class="sxs-lookup"><span data-stu-id="f5a16-112">A pointer to the handle of the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a16-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5a16-113">Return value</span></span>

<span data-ttu-id="f5a16-114">如果函式成功 (使用者選取 NIC) ，傳回值會 NMERR \_ 成功，而且 *phBlob* 指向的 BLOB 會填入。</span><span class="sxs-lookup"><span data-stu-id="f5a16-114">If the function is successful (the user selects a NIC), the return value is NMERR\_SUCCESS, and the BLOB that *phBlob* points to is filled in.</span></span>

<span data-ttu-id="f5a16-115">如果使用者未選取 NIC，則傳回值為 **NMERR \_ NO \_ NPP \_ SELECTED**。</span><span class="sxs-lookup"><span data-stu-id="f5a16-115">If the user does not select an NIC, the return value is **NMERR\_NO\_NPP\_SELECTED**.</span></span>

<span data-ttu-id="f5a16-116">如果函式不成功，則傳回值為另一個 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="f5a16-116">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a16-117">備註</span><span class="sxs-lookup"><span data-stu-id="f5a16-117">Remarks</span></span>

<span data-ttu-id="f5a16-118">當呼叫時，網路監視器會顯示 [ **選取網路** ] 對話方塊，您可以使用此對話方塊來選取 NIC。</span><span class="sxs-lookup"><span data-stu-id="f5a16-118">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="f5a16-119">代表 NIC 的 NPP BLOB 會傳回給呼叫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f5a16-119">The NPP BLOB that represents the NIC is returned to the calling application.</span></span>

<span data-ttu-id="f5a16-120">如果以 *hFilterBlob* 命名的 blob 是 [*特殊的 blob*](s.md)，則搜尋工具會嘗試處理它。</span><span class="sxs-lookup"><span data-stu-id="f5a16-120">If the BLOB named by *hFilterBlob* is a [*special BLOB*](s.md), the finder will attempt to process it.</span></span> <span data-ttu-id="f5a16-121">例如，先前從遠端 NPP 傳回特殊 BLOB 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f5a16-121">An example would be a call that had previously returned a special BLOB from the remote NPP.</span></span> <span data-ttu-id="f5a16-122">應用程式已插入必要的標記、電腦 \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="f5a16-122">The application inserted the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="f5a16-123">在這種情況下，搜尋工具會將此 BLOB 傳遞到遠端 NPP，然後傳回 NPP Blob 的表格，代表所要求的電腦。</span><span class="sxs-lookup"><span data-stu-id="f5a16-123">In this situation, the finder would pass this BLOB to the remote NPP, which would then return a table of NPP BLOBs representing the machine requested.</span></span> <span data-ttu-id="f5a16-124">這些遠端 NPP Blob 將會出現在對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="f5a16-124">These remote NPP BLOBs would appear in the dialog box.</span></span>

<span data-ttu-id="f5a16-125">呼叫端必須呼叫 [DestroyBlob](destroyblob.md) 函式，此函式會在不再需要時終結傳回的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="f5a16-125">The caller must call the [DestroyBlob](destroyblob.md) function, which destroys the returned BLOB when it is no longer required.</span></span>



| <span data-ttu-id="f5a16-126">如需下列項目的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="f5a16-126">For more information about</span></span> | <span data-ttu-id="f5a16-127">請參閱</span><span class="sxs-lookup"><span data-stu-id="f5a16-127">See</span></span>                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f5a16-128">選取 Nic 的三種方式</span><span class="sxs-lookup"><span data-stu-id="f5a16-128">Three ways to select NICs</span></span>  | [<span data-ttu-id="f5a16-129">選取網路介面卡</span><span class="sxs-lookup"><span data-stu-id="f5a16-129">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |
| <span data-ttu-id="f5a16-130">指定篩選 BLOB</span><span class="sxs-lookup"><span data-stu-id="f5a16-130">Specifying a filter BLOB</span></span>   | [<span data-ttu-id="f5a16-131">指定篩選 BLOB</span><span class="sxs-lookup"><span data-stu-id="f5a16-131">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a><span data-ttu-id="f5a16-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5a16-132">Requirements</span></span>



| <span data-ttu-id="f5a16-133">需求</span><span class="sxs-lookup"><span data-stu-id="f5a16-133">Requirement</span></span> | <span data-ttu-id="f5a16-134">值</span><span class="sxs-lookup"><span data-stu-id="f5a16-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a16-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5a16-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a16-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5a16-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f5a16-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5a16-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a16-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5a16-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5a16-139">標頭</span><span class="sxs-lookup"><span data-stu-id="f5a16-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a16-140"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f5a16-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="f5a16-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="f5a16-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5a16-142"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5a16-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5a16-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f5a16-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5a16-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5a16-144"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a16-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5a16-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a16-146">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="f5a16-146">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="f5a16-147">SelectNPPBlobFromTable</span><span class="sxs-lookup"><span data-stu-id="f5a16-147">SelectNPPBlobFromTable</span></span>](selectnppblobfromtable.md)
</dt> </dl>

 

 




