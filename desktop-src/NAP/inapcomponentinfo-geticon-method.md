---
title: 'INapComponentInfo GetIcon 方法 (NapCommon .h) '
description: NAP 系統會使用它來取得健全狀況用戶端的圖示。
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- GetIcon 方法 NAP
- GetIcon 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，GetIcon 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934991"
---
# <a name="inapcomponentinfogeticon-method"></a><span data-ttu-id="cb437-106">INapComponentInfo：： GetIcon 方法</span><span class="sxs-lookup"><span data-stu-id="cb437-106">INapComponentInfo::GetIcon method</span></span>

> [!Note]  
> <span data-ttu-id="cb437-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="cb437-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cb437-108">**INapComponentInfo：： GetIcon** 回呼方法是由 NAP 系統用來取得健全狀況用戶端的圖示。</span><span class="sxs-lookup"><span data-stu-id="cb437-108">The **INapComponentInfo::GetIcon** callback method is used by the NAP System to get the icon of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb437-109">語法</span><span class="sxs-lookup"><span data-stu-id="cb437-109">Syntax</span></span>


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a><span data-ttu-id="cb437-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb437-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb437-111">*dllFilePath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cb437-111">*dllFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb437-112">指向 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) 指標的指標，用來傳回包含圖示之 DLL 的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="cb437-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) used to return the file path of the DLL that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="cb437-113">*iconResourceId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cb437-113">*iconResourceId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb437-114">值的指標，用來傳回要使用之圖示的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb437-114">A pointer to value used to return the resource ID of the icon to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb437-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb437-115">Return value</span></span>

<span data-ttu-id="cb437-116">根據此作業的結果傳回這些錯誤碼的其中一個。</span><span class="sxs-lookup"><span data-stu-id="cb437-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="cb437-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cb437-117">Return code</span></span>                                                                                     | <span data-ttu-id="cb437-118">Description</span><span class="sxs-lookup"><span data-stu-id="cb437-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb437-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cb437-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="cb437-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="cb437-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="cb437-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="cb437-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="cb437-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="cb437-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="cb437-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cb437-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="cb437-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="cb437-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb437-125">備註</span><span class="sxs-lookup"><span data-stu-id="cb437-125">Remarks</span></span>

<span data-ttu-id="cb437-126">您應該根據呼叫端的語言識別項來當地語系化圖示。</span><span class="sxs-lookup"><span data-stu-id="cb437-126">Icons should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb437-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb437-127">Requirements</span></span>



| <span data-ttu-id="cb437-128">需求</span><span class="sxs-lookup"><span data-stu-id="cb437-128">Requirement</span></span> | <span data-ttu-id="cb437-129">值</span><span class="sxs-lookup"><span data-stu-id="cb437-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb437-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb437-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cb437-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb437-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cb437-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb437-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cb437-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb437-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cb437-134">標頭</span><span class="sxs-lookup"><span data-stu-id="cb437-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb437-135"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb437-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb437-136">Idl</span><span class="sxs-lookup"><span data-stu-id="cb437-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb437-137"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb437-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb437-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb437-138">See also</span></span>

<dl> <span data-ttu-id="cb437-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="cb437-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="cb437-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="cb437-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





