---
title: 'INapComponentConfig3 >newconfig.json 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供一種方式來建立特定設定識別碼的設定資料。
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- '>newconfig.json 方法 NAP'
- '>newconfig.json 方法 NAP，INapComponentConfig3 介面'
- INapComponentConfig3 介面 NAP，>newconfig.json 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094247"
---
# <a name="inapcomponentconfig3newconfig-method"></a><span data-ttu-id="96076-106">INapComponentConfig3：： >newconfig.json 方法</span><span class="sxs-lookup"><span data-stu-id="96076-106">INapComponentConfig3::NewConfig method</span></span>

> [!Note]  
> <span data-ttu-id="96076-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="96076-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="96076-108">**>newconfig.json** 方法是由系統健康狀態驗證 (shv) 來提供一種方法，以建立特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="96076-108">The **NewConfig** method is implemented by system health validators (SHVs) to provide a way to create configuration data for a specific configuration ID.</span></span> <span data-ttu-id="96076-109">呼叫此函式時，SHV 必須配置新的設定資料，並填入預設設定資料的複本。</span><span class="sxs-lookup"><span data-stu-id="96076-109">When this function is called, an SHV must allocate new configuration data and populate it with a copy of the default configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="96076-110">語法</span><span class="sxs-lookup"><span data-stu-id="96076-110">Syntax</span></span>


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="96076-111">參數</span><span class="sxs-lookup"><span data-stu-id="96076-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96076-112">*configID*</span><span class="sxs-lookup"><span data-stu-id="96076-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="96076-113">表示設定的值。</span><span class="sxs-lookup"><span data-stu-id="96076-113">A value that represents the configuration.</span></span> <span data-ttu-id="96076-114">網路原則伺服器 (NPS) 服務指派 *ConfigID* ，且在 SHV 內是唯一的。</span><span class="sxs-lookup"><span data-stu-id="96076-114">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96076-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="96076-115">Return value</span></span>

<span data-ttu-id="96076-116">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="96076-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="96076-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="96076-117">Return code</span></span>                                                                                                 | <span data-ttu-id="96076-118">Description</span><span class="sxs-lookup"><span data-stu-id="96076-118">Description</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96076-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="96076-119"><dt>**S\_OK** </dt></span></span> </dl>                       | <span data-ttu-id="96076-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="96076-120">The operation is successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="96076-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="96076-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="96076-122">*ConfigID* 為 0 (保留給預設設定) 的值。</span><span class="sxs-lookup"><span data-stu-id="96076-122">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/>                  |
| <dl> <span data-ttu-id="96076-123"><dt>**NAP \_ E \_ SHV 設定已 \_ \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="96076-123"><dt>**NAP\_E\_SHV\_CONFIG\_EXISTED**</dt></span></span> </dl> | <span data-ttu-id="96076-124">*ConfigID* 已經存在。</span><span class="sxs-lookup"><span data-stu-id="96076-124">*ConfigID* already exists.</span></span> <span data-ttu-id="96076-125">NPS 已知的識別碼清單與 SHV 不同。</span><span class="sxs-lookup"><span data-stu-id="96076-125">The list of IDs known to NPS is different from the SHV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96076-126">備註</span><span class="sxs-lookup"><span data-stu-id="96076-126">Remarks</span></span>

<span data-ttu-id="96076-127">**>newconfig.json** 建立新的設定之後，應該使用 [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md)、 [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)和 [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)方法來視需要變更設定。</span><span class="sxs-lookup"><span data-stu-id="96076-127">After the new configuration is created by **NewConfig**, the [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md), and [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) methods should be used to alter the configuration as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="96076-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="96076-128">Requirements</span></span>



| <span data-ttu-id="96076-129">需求</span><span class="sxs-lookup"><span data-stu-id="96076-129">Requirement</span></span> | <span data-ttu-id="96076-130">值</span><span class="sxs-lookup"><span data-stu-id="96076-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96076-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96076-131">Minimum supported client</span></span><br/> | <span data-ttu-id="96076-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="96076-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="96076-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96076-133">Minimum supported server</span></span><br/> | <span data-ttu-id="96076-134">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96076-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96076-135">標頭</span><span class="sxs-lookup"><span data-stu-id="96076-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="96076-136"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="96076-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="96076-137">Idl</span><span class="sxs-lookup"><span data-stu-id="96076-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96076-138"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="96076-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96076-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96076-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96076-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="96076-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





