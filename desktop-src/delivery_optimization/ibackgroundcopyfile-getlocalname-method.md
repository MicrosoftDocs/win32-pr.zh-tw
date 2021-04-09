---
title: 'IBackgroundCopyFile GetLocalName 方法 (>deliveryoptimization .h) '
description: 抓取檔案的本機名稱。
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- GetLocalName 方法
- GetLocalName 方法，IBackgroundCopyFile 介面
- IBackgroundCopyFile 介面，GetLocalName 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025011"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a><span data-ttu-id="45790-106">IBackgroundCopyFile：： GetLocalName 方法</span><span class="sxs-lookup"><span data-stu-id="45790-106">IBackgroundCopyFile::GetLocalName method</span></span>

<span data-ttu-id="45790-107">抓取檔案的本機名稱。</span><span class="sxs-lookup"><span data-stu-id="45790-107">Retrieves the local name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="45790-108">語法</span><span class="sxs-lookup"><span data-stu-id="45790-108">Syntax</span></span>


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="45790-109">參數</span><span class="sxs-lookup"><span data-stu-id="45790-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45790-110">*ppName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="45790-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45790-111">以 Null 終止的字串，其中包含用戶端上的檔案名。</span><span class="sxs-lookup"><span data-stu-id="45790-111">Null-terminated string that contains the name of the file on the client.</span></span> <span data-ttu-id="45790-112">名稱是完整的。</span><span class="sxs-lookup"><span data-stu-id="45790-112">The name is fully qualified.</span></span> <span data-ttu-id="45790-113">完成時，呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式以釋放 *ppName* 。</span><span class="sxs-lookup"><span data-stu-id="45790-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45790-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="45790-114">Return value</span></span>

<span data-ttu-id="45790-115">這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="45790-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="45790-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="45790-116">Requirements</span></span>



| <span data-ttu-id="45790-117">需求</span><span class="sxs-lookup"><span data-stu-id="45790-117">Requirement</span></span> | <span data-ttu-id="45790-118">值</span><span class="sxs-lookup"><span data-stu-id="45790-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45790-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45790-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45790-120">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45790-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="45790-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45790-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45790-122">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45790-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="45790-123">標頭</span><span class="sxs-lookup"><span data-stu-id="45790-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="45790-124"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="45790-124"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="45790-125">Idl</span><span class="sxs-lookup"><span data-stu-id="45790-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45790-126"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="45790-126"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="45790-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="45790-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="45790-128"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="45790-128"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="45790-129">DLL</span><span class="sxs-lookup"><span data-stu-id="45790-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45790-130"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45790-130"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="45790-131">IID</span><span class="sxs-lookup"><span data-stu-id="45790-131">IID</span></span><br/>                      | <span data-ttu-id="45790-132">IID_IBackgroundCopyFile 定義為01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="45790-132">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="45790-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45790-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45790-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="45790-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="45790-135">**IBackgroundCopyFile::GetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="45790-135">**IBackgroundCopyFile::GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

