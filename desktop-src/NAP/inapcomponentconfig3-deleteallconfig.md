---
title: 'INapComponentConfig3 DeleteAllConfig 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供在安裝之後將 SHV 存放區重設為其原始狀態的方法。
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- DeleteAllConfig 方法 NAP
- DeleteAllConfig 方法 NAP，INapComponentConfig3 介面
- INapComponentConfig3 介面 NAP，DeleteAllConfig 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843336"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a><span data-ttu-id="75ee1-106">INapComponentConfig3：:D eleteAllConfig 方法</span><span class="sxs-lookup"><span data-stu-id="75ee1-106">INapComponentConfig3::DeleteAllConfig method</span></span>

> [!Note]  
> <span data-ttu-id="75ee1-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="75ee1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="75ee1-108">**DeleteAllConfig** 方法是由系統健康狀態驗證 (shv) 來提供在安裝之後，將 SHV 存放區重設為其原始狀態的方法。</span><span class="sxs-lookup"><span data-stu-id="75ee1-108">The **DeleteAllConfig** method is implemented by system health validators (SHVs) to provide a way to reset the SHV store to its original state after setup.</span></span> <span data-ttu-id="75ee1-109">所有設定資料（預設設定除外）都必須刪除。</span><span class="sxs-lookup"><span data-stu-id="75ee1-109">All configuration data except for the default configuration must be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ee1-110">語法</span><span class="sxs-lookup"><span data-stu-id="75ee1-110">Syntax</span></span>


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a><span data-ttu-id="75ee1-111">參數</span><span class="sxs-lookup"><span data-stu-id="75ee1-111">Parameters</span></span>

<span data-ttu-id="75ee1-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="75ee1-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75ee1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="75ee1-113">Return value</span></span>

<span data-ttu-id="75ee1-114">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="75ee1-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="75ee1-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="75ee1-115">Return code</span></span>                                                                           | <span data-ttu-id="75ee1-116">Description</span><span class="sxs-lookup"><span data-stu-id="75ee1-116">Description</span></span>                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="75ee1-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="75ee1-117"><dt>**S\_OK** </dt></span></span> </dl> | <span data-ttu-id="75ee1-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="75ee1-118">The operation is successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75ee1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="75ee1-119">Requirements</span></span>



| <span data-ttu-id="75ee1-120">需求</span><span class="sxs-lookup"><span data-stu-id="75ee1-120">Requirement</span></span> | <span data-ttu-id="75ee1-121">值</span><span class="sxs-lookup"><span data-stu-id="75ee1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ee1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75ee1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="75ee1-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="75ee1-123">None supported</span></span><br/>                                                                |
| <span data-ttu-id="75ee1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75ee1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="75ee1-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75ee1-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75ee1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="75ee1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ee1-127"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="75ee1-127"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="75ee1-128">Idl</span><span class="sxs-lookup"><span data-stu-id="75ee1-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75ee1-129"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="75ee1-129"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ee1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75ee1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ee1-131">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="75ee1-131">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





