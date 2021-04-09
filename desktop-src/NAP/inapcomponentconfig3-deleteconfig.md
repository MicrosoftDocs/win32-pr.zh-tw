---
title: 'INapComponentConfig3 DeleteConfig 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供一種方式來刪除特定設定識別碼的設定資料。
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- DeleteConfig 方法 NAP
- DeleteConfig 方法 NAP，INapComponentConfig3 介面
- INapComponentConfig3 介面 NAP，DeleteConfig 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685769"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a><span data-ttu-id="c04a8-106">INapComponentConfig3：:D eleteConfig 方法</span><span class="sxs-lookup"><span data-stu-id="c04a8-106">INapComponentConfig3::DeleteConfig method</span></span>

> [!Note]  
> <span data-ttu-id="c04a8-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="c04a8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c04a8-108">**DeleteConfig** 方法是由系統健康狀態驗證 (shv) 來提供一種方式，以刪除特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="c04a8-108">The **DeleteConfig** method is implemented by system health validators (SHVs) to provide a way to delete configuration data for a specific configuration ID.</span></span> <span data-ttu-id="c04a8-109">刪除設定資料之後，可能會重複使用此識別碼。</span><span class="sxs-lookup"><span data-stu-id="c04a8-109">The ID may be reused after the configuration data has been deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="c04a8-110">語法</span><span class="sxs-lookup"><span data-stu-id="c04a8-110">Syntax</span></span>


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="c04a8-111">參數</span><span class="sxs-lookup"><span data-stu-id="c04a8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c04a8-112">*configID*</span><span class="sxs-lookup"><span data-stu-id="c04a8-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="c04a8-113">值，表示要刪除的設定資料。</span><span class="sxs-lookup"><span data-stu-id="c04a8-113">A value that represents the configuration data to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c04a8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c04a8-114">Return value</span></span>

<span data-ttu-id="c04a8-115">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c04a8-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="c04a8-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c04a8-116">Return code</span></span>                                                                                                    | <span data-ttu-id="c04a8-117">Description</span><span class="sxs-lookup"><span data-stu-id="c04a8-117">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c04a8-118"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c04a8-118"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="c04a8-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c04a8-119">The operation is successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="c04a8-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c04a8-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="c04a8-121">*ConfigID* 為 0 (保留給預設設定) 的值。</span><span class="sxs-lookup"><span data-stu-id="c04a8-121">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/> |
| <dl> <span data-ttu-id="c04a8-122"><dt>**\_ \_ \_ \_ \_ 找不到 NAP E SHV 設定**</dt></span><span class="sxs-lookup"><span data-stu-id="c04a8-122"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="c04a8-123">找不到 *ConfigID* 。</span><span class="sxs-lookup"><span data-stu-id="c04a8-123">*ConfigID* cannot be found.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="c04a8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c04a8-124">Requirements</span></span>



| <span data-ttu-id="c04a8-125">需求</span><span class="sxs-lookup"><span data-stu-id="c04a8-125">Requirement</span></span> | <span data-ttu-id="c04a8-126">值</span><span class="sxs-lookup"><span data-stu-id="c04a8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c04a8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c04a8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c04a8-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="c04a8-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c04a8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c04a8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c04a8-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c04a8-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c04a8-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c04a8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c04a8-132"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="c04a8-132"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c04a8-133">Idl</span><span class="sxs-lookup"><span data-stu-id="c04a8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c04a8-134"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c04a8-134"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c04a8-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c04a8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04a8-136">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="c04a8-136">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





