---
title: 'CreateConnectionOptions 方法 (WSManDisp .h) '
description: 建立 ConnectionOptions 物件，這個物件會指定建立會話時使用的使用者名稱和密碼。
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- CreateConnectionOptions 方法 Windows 遠端管理
- CreateConnectionOptions 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，CreateConnectionOptions 方法
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843312"
---
# <a name="wsmancreateconnectionoptions-method"></a><span data-ttu-id="077ff-106">WSMan. CreateConnectionOptions 方法</span><span class="sxs-lookup"><span data-stu-id="077ff-106">WSMan.CreateConnectionOptions method</span></span>

<span data-ttu-id="077ff-107">建立 [**ConnectionOptions**](connectionoptions.md) 物件，這個物件會指定建立會話時使用的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="077ff-107">Creates a [**ConnectionOptions**](connectionoptions.md) object that specifies the user name and password used when creating a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="077ff-108">語法</span><span class="sxs-lookup"><span data-stu-id="077ff-108">Syntax</span></span>


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a><span data-ttu-id="077ff-109">參數</span><span class="sxs-lookup"><span data-stu-id="077ff-109">Parameters</span></span>

<span data-ttu-id="077ff-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="077ff-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="077ff-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="077ff-111">Return value</span></span>

<span data-ttu-id="077ff-112">用來指定使用者名稱和密碼組的 [**ConnectionOptions**](connectionoptions.md) 物件，用來識別要驗證的使用者。</span><span class="sxs-lookup"><span data-stu-id="077ff-112">A [**ConnectionOptions**](connectionoptions.md) object used to specify a user name and password pair that is used to identify a user for authentication.</span></span>

## <a name="remarks"></a><span data-ttu-id="077ff-113">備註</span><span class="sxs-lookup"><span data-stu-id="077ff-113">Remarks</span></span>

<span data-ttu-id="077ff-114">下列語法用來呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="077ff-114">The following syntax is used to call this method.</span></span>


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a><span data-ttu-id="077ff-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="077ff-115">Requirements</span></span>



| <span data-ttu-id="077ff-116">需求</span><span class="sxs-lookup"><span data-stu-id="077ff-116">Requirement</span></span> | <span data-ttu-id="077ff-117">值</span><span class="sxs-lookup"><span data-stu-id="077ff-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="077ff-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="077ff-118">Minimum supported client</span></span><br/> | <span data-ttu-id="077ff-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="077ff-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="077ff-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="077ff-120">Minimum supported server</span></span><br/> | <span data-ttu-id="077ff-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="077ff-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="077ff-122">標頭</span><span class="sxs-lookup"><span data-stu-id="077ff-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="077ff-123"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="077ff-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="077ff-124">Idl</span><span class="sxs-lookup"><span data-stu-id="077ff-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="077ff-125"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="077ff-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="077ff-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="077ff-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="077ff-127"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="077ff-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="077ff-128">DLL</span><span class="sxs-lookup"><span data-stu-id="077ff-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="077ff-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="077ff-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="077ff-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="077ff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="077ff-131">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="077ff-131">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="077ff-132">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="077ff-132">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





