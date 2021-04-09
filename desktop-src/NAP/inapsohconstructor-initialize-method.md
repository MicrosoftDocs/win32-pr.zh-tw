---
title: 'INapSoHConstructor Initialize 方法 (NapProtocol .h) '
description: 初始化 NAP 系統中的 SoH 通訊協定封包。
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapSoHConstructor 介面
- INapSoHConstructor 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934303"
---
# <a name="inapsohconstructorinitialize-method"></a><span data-ttu-id="ee5ff-106">INapSoHConstructor：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="ee5ff-106">INapSoHConstructor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="ee5ff-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="ee5ff-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ee5ff-108">**INapSoHConstructor：： Initialize** 方法會初始化 NAP 系統中的 SoH 通訊協定封包。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-108">The **INapSoHConstructor::Initialize** method initializes a SoH protocol packet in the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee5ff-109">語法</span><span class="sxs-lookup"><span data-stu-id="ee5ff-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="ee5ff-110">參數</span><span class="sxs-lookup"><span data-stu-id="ee5ff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee5ff-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="ee5ff-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee5ff-112">唯一的 [SystemHealthEntityId](nap-datatypes.md) ，其中包含正在建立封包的 SHA 或 SHV 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that is constructing the packet.</span></span>

</dd> <dt>

<span data-ttu-id="ee5ff-113">*isRequest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee5ff-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee5ff-114">如果封包是 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林\*\*\*\*值為 TRUE** ，如果是 **SoHResponse**，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-114">A **BOOL** that is **TRUE** if the packet is to be an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is to be an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee5ff-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee5ff-115">Return value</span></span>

<span data-ttu-id="ee5ff-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ee5ff-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ee5ff-117">Return code</span></span>                                                                                     | <span data-ttu-id="ee5ff-118">Description</span><span class="sxs-lookup"><span data-stu-id="ee5ff-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee5ff-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ee5ff-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ee5ff-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ee5ff-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ee5ff-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ee5ff-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ee5ff-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ee5ff-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ee5ff-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee5ff-125">備註</span><span class="sxs-lookup"><span data-stu-id="ee5ff-125">Remarks</span></span>

<span data-ttu-id="ee5ff-126">每個封包都必須剛好呼叫這個方法一次。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-126">This method must be called exactly once per packet.</span></span>

<span data-ttu-id="ee5ff-127">在 *識別碼* 中指定的 [SystemHealthEntityId](nap-datatypes.md)是新建立的 SOH 封包中的第一個 TLV，而且具有屬性類型 [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)。</span><span class="sxs-lookup"><span data-stu-id="ee5ff-127">The [SystemHealthEntityId](nap-datatypes.md) specified in *id*, is the first TLV in the newly constructed SOH packet and has the attribute type [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee5ff-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee5ff-128">Requirements</span></span>



| <span data-ttu-id="ee5ff-129">需求</span><span class="sxs-lookup"><span data-stu-id="ee5ff-129">Requirement</span></span> | <span data-ttu-id="ee5ff-130">值</span><span class="sxs-lookup"><span data-stu-id="ee5ff-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee5ff-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee5ff-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ee5ff-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee5ff-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee5ff-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee5ff-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ee5ff-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee5ff-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ee5ff-135">標頭</span><span class="sxs-lookup"><span data-stu-id="ee5ff-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee5ff-136"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee5ff-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee5ff-137">Idl</span><span class="sxs-lookup"><span data-stu-id="ee5ff-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee5ff-138"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee5ff-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="ee5ff-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ee5ff-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee5ff-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee5ff-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ee5ff-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee5ff-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee5ff-142">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="ee5ff-142">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





