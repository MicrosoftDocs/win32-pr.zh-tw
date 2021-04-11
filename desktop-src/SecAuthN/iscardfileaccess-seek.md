---
description: Seek 方法會選取從中進行 (讀取/寫入) 存取的物件。
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: ISCardFileAccess：： Seek 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693228"
---
# <a name="iscardfileaccessseek-method"></a><span data-ttu-id="69943-103">ISCardFileAccess：： Seek 方法</span><span class="sxs-lookup"><span data-stu-id="69943-103">ISCardFileAccess::Seek method</span></span>

<span data-ttu-id="69943-104">\[**Seek** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="69943-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="69943-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="69943-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="69943-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="69943-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="69943-107">**Seek** 方法會選取從中進行 (讀取/寫入) 存取的物件。</span><span class="sxs-lookup"><span data-stu-id="69943-107">The **Seek** method selects the object from which (read/write) access will be done.</span></span>

## <a name="syntax"></a><span data-ttu-id="69943-108">語法</span><span class="sxs-lookup"><span data-stu-id="69943-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a><span data-ttu-id="69943-109">參數</span><span class="sxs-lookup"><span data-stu-id="69943-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69943-110">*hFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69943-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69943-111">開啟檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="69943-111">Handle of the open file.</span></span>

</dd> <dt>

<span data-ttu-id="69943-112">*搜尋* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69943-112">*Seek* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69943-113">應開始搜尋的位置。</span><span class="sxs-lookup"><span data-stu-id="69943-113">Location where the seek should begin.</span></span>



| <span data-ttu-id="69943-114">值</span><span class="sxs-lookup"><span data-stu-id="69943-114">Value</span></span>                                                                                                | <span data-ttu-id="69943-115">意義</span><span class="sxs-lookup"><span data-stu-id="69943-115">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="69943-116"><dt>SC \_ SEEK \_ \_ 開頭</dt></span><span class="sxs-lookup"><span data-stu-id="69943-116"><dt>SC\_SEEK\_FROM\_BEGINNING</dt></span></span> </dl> | <span data-ttu-id="69943-117">開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="69943-117">Begin search at the beginning.</span></span><br/>          |
| <dl> <span data-ttu-id="69943-118"><dt>SC \_ SEEK \_ FROM \_ END </dt></span><span class="sxs-lookup"><span data-stu-id="69943-118"><dt>SC\_SEEK\_FROM\_END </dt></span></span> </dl>      | <span data-ttu-id="69943-119">從結尾開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="69943-119">Begin search from the end.</span></span><br/>              |
| <dl> <span data-ttu-id="69943-120"><dt>SC \_ SEEK \_ 相對</dt></span><span class="sxs-lookup"><span data-stu-id="69943-120"><dt>SC\_SEEK\_RELATIVE</dt></span></span> </dl>        | <span data-ttu-id="69943-121">從目前的位置開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="69943-121">Begin search from the current position.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="69943-122">*lOffset* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69943-122">*lOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69943-123">參考物件中的資料物件數目。</span><span class="sxs-lookup"><span data-stu-id="69943-123">Number of data objects from the reference object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69943-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="69943-124">Return value</span></span>

<span data-ttu-id="69943-125">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="69943-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="69943-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="69943-126">Return code</span></span>                                                                                   | <span data-ttu-id="69943-127">Description</span><span class="sxs-lookup"><span data-stu-id="69943-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="69943-128"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="69943-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="69943-129">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="69943-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="69943-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="69943-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="69943-131">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="69943-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="69943-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="69943-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="69943-133">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="69943-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="69943-134">備註</span><span class="sxs-lookup"><span data-stu-id="69943-134">Remarks</span></span>

<span data-ttu-id="69943-135">若要讀取或寫入檔案，請分別呼叫 [**讀取**](iscardfileaccess-read.md) 或 [**寫入**](iscardfileaccess-write.md) 。</span><span class="sxs-lookup"><span data-stu-id="69943-135">To read to or write from a file, call [**Read**](iscardfileaccess-read.md) or [**Write**](iscardfileaccess-write.md) respectively.</span></span>

<span data-ttu-id="69943-136">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="69943-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="69943-137">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="69943-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="69943-138">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="69943-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69943-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="69943-139">Requirements</span></span>



| <span data-ttu-id="69943-140">需求</span><span class="sxs-lookup"><span data-stu-id="69943-140">Requirement</span></span> | <span data-ttu-id="69943-141">值</span><span class="sxs-lookup"><span data-stu-id="69943-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69943-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69943-142">Minimum supported client</span></span><br/> | <span data-ttu-id="69943-143">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69943-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="69943-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69943-144">Minimum supported server</span></span><br/> | <span data-ttu-id="69943-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69943-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="69943-146">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="69943-146">End of client support</span></span><br/>    | <span data-ttu-id="69943-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="69943-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="69943-148">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="69943-148">End of server support</span></span><br/>    | <span data-ttu-id="69943-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69943-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="69943-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69943-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69943-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="69943-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="69943-152">**讀**</span><span class="sxs-lookup"><span data-stu-id="69943-152">**Read**</span></span>](iscardfileaccess-read.md)
</dt> <dt>

[<span data-ttu-id="69943-153">**寫**</span><span class="sxs-lookup"><span data-stu-id="69943-153">**Write**</span></span>](iscardfileaccess-write.md)
</dt> </dl>

 

 
