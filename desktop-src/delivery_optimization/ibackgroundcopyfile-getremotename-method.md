---
title: 'IBackgroundCopyFile GetRemoteName 方法 (>deliveryoptimization .h) '
description: 抓取檔案的遠端名稱。
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- GetRemoteName 方法
- GetRemoteName 方法，IBackgroundCopyFile 介面
- IBackgroundCopyFile 介面，GetRemoteName 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025009"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a><span data-ttu-id="3ec92-106">IBackgroundCopyFile：： GetRemoteName 方法</span><span class="sxs-lookup"><span data-stu-id="3ec92-106">IBackgroundCopyFile::GetRemoteName method</span></span>

<span data-ttu-id="3ec92-107">抓取檔案的遠端名稱。</span><span class="sxs-lookup"><span data-stu-id="3ec92-107">Retrieves the remote name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec92-108">語法</span><span class="sxs-lookup"><span data-stu-id="3ec92-108">Syntax</span></span>


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="3ec92-109">參數</span><span class="sxs-lookup"><span data-stu-id="3ec92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec92-110">*ppName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ec92-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ec92-111">以 Null 終止的字串，其中包含要傳送之檔案的遠端名稱。</span><span class="sxs-lookup"><span data-stu-id="3ec92-111">Null-terminated string that contains the remote name of the file to transfer.</span></span> <span data-ttu-id="3ec92-112">名稱是完整的。</span><span class="sxs-lookup"><span data-stu-id="3ec92-112">The name is fully qualified.</span></span> <span data-ttu-id="3ec92-113">完成時，呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式以釋放 *ppName* 。</span><span class="sxs-lookup"><span data-stu-id="3ec92-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ec92-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ec92-114">Return value</span></span>

<span data-ttu-id="3ec92-115">這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3ec92-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ec92-116">備註</span><span class="sxs-lookup"><span data-stu-id="3ec92-116">Remarks</span></span>

<span data-ttu-id="3ec92-117">若要變更遠端檔案名，請呼叫 [**IBackgroundCopyFile2：： SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3ec92-117">To change the remote file name, call the [**IBackgroundCopyFile2::SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec92-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ec92-118">Requirements</span></span>



| <span data-ttu-id="3ec92-119">需求</span><span class="sxs-lookup"><span data-stu-id="3ec92-119">Requirement</span></span> | <span data-ttu-id="3ec92-120">值</span><span class="sxs-lookup"><span data-stu-id="3ec92-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec92-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ec92-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec92-122">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec92-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3ec92-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ec92-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec92-124">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec92-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3ec92-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3ec92-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec92-126"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ec92-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ec92-127">Idl</span><span class="sxs-lookup"><span data-stu-id="3ec92-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ec92-128"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ec92-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ec92-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ec92-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ec92-130"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ec92-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3ec92-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3ec92-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ec92-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ec92-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3ec92-133">IID</span><span class="sxs-lookup"><span data-stu-id="3ec92-133">IID</span></span><br/>                      | <span data-ttu-id="3ec92-134">IID_IBackgroundCopyFile 定義為01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="3ec92-134">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="3ec92-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ec92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec92-136">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="3ec92-136">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="3ec92-137">**IBackgroundCopyFile：： GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="3ec92-137">**IBackgroundCopyFile::GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

