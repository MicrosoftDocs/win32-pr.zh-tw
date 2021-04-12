---
description: Read 方法會從指定的檔案讀取並傳回指定的資料。
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: ISCardFileAccess：： Read 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192957"
---
# <a name="iscardfileaccessread-method"></a><span data-ttu-id="4bc96-103">ISCardFileAccess：： Read 方法</span><span class="sxs-lookup"><span data-stu-id="4bc96-103">ISCardFileAccess::Read method</span></span>

<span data-ttu-id="4bc96-104">\[**Read** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4bc96-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4bc96-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="4bc96-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4bc96-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4bc96-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4bc96-107">**Read** 方法會從指定的檔案讀取並傳回指定的資料。</span><span class="sxs-lookup"><span data-stu-id="4bc96-107">The **Read** method reads and returns the specified data from a given file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc96-108">語法</span><span class="sxs-lookup"><span data-stu-id="4bc96-108">Syntax</span></span>


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="4bc96-109">參數</span><span class="sxs-lookup"><span data-stu-id="4bc96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bc96-110">*hFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bc96-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc96-111">要存取的開啟檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4bc96-111">Handle of the open file to access.</span></span>

</dd> <dt>

<span data-ttu-id="4bc96-112">*lBytesToRead* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bc96-112">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc96-113">要讀取的資料長度 () 或讀取 () 輸出的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4bc96-113">Length of data to be read (in) or number of bytes read (out).</span></span> <span data-ttu-id="4bc96-114">傳回 Bstr 陣列形式的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="4bc96-114">Returns list of files as an array of BSTRs.</span></span>

</dd> <dt>

<span data-ttu-id="4bc96-115">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bc96-115">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc96-116">指定是否應使用安全訊息。</span><span class="sxs-lookup"><span data-stu-id="4bc96-116">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="4bc96-117">**SC \_ FL \_ 安全 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="4bc96-117">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4bc96-118">*ppBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4bc96-118">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc96-119">包含讀取資料的 [**IByteBuffer**](ibytebuffer.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4bc96-119">An [**IByteBuffer**](ibytebuffer.md) object containing the read data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bc96-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bc96-120">Return value</span></span>

<span data-ttu-id="4bc96-121">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="4bc96-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4bc96-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4bc96-122">Return code</span></span>                                                                                   | <span data-ttu-id="4bc96-123">Description</span><span class="sxs-lookup"><span data-stu-id="4bc96-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4bc96-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc96-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4bc96-125">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="4bc96-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4bc96-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc96-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4bc96-127">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="4bc96-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="4bc96-128"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc96-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4bc96-129">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="4bc96-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="4bc96-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc96-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4bc96-131">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="4bc96-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="4bc96-132">備註</span><span class="sxs-lookup"><span data-stu-id="4bc96-132">Remarks</span></span>

<span data-ttu-id="4bc96-133">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="4bc96-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="4bc96-134">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4bc96-134">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4bc96-135">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="4bc96-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc96-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bc96-136">Requirements</span></span>



| <span data-ttu-id="4bc96-137">需求</span><span class="sxs-lookup"><span data-stu-id="4bc96-137">Requirement</span></span> | <span data-ttu-id="4bc96-138">值</span><span class="sxs-lookup"><span data-stu-id="4bc96-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4bc96-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bc96-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4bc96-140">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bc96-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4bc96-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bc96-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4bc96-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bc96-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4bc96-143">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4bc96-143">End of client support</span></span><br/>    | <span data-ttu-id="4bc96-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4bc96-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="4bc96-145">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4bc96-145">End of server support</span></span><br/>    | <span data-ttu-id="4bc96-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4bc96-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="4bc96-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bc96-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc96-148">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="4bc96-148">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
