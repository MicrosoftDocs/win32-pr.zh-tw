---
title: ITSRemoteProgram3 ServerStartApp 方法
description: 指定要在遠端會話中啟動的應用程式。
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- ServerStartApp 方法遠端桌面服務
- ServerStartApp 方法遠端桌面服務，ITSRemoteProgram3 介面
- ITSRemoteProgram3 介面遠端桌面服務，ServerStartApp 方法
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970450"
---
# <a name="itsremoteprogram3serverstartapp-method"></a><span data-ttu-id="3c8e0-106">ITSRemoteProgram3：： ServerStartApp 方法</span><span class="sxs-lookup"><span data-stu-id="3c8e0-106">ITSRemoteProgram3::ServerStartApp method</span></span>

<span data-ttu-id="3c8e0-107">指定要在遠端會話中啟動的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c8e0-107">Specifies an App to start in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8e0-108">語法</span><span class="sxs-lookup"><span data-stu-id="3c8e0-108">Syntax</span></span>


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="3c8e0-109">參數</span><span class="sxs-lookup"><span data-stu-id="3c8e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8e0-110">*bstrAppUserModelId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c8e0-110">*bstrAppUserModelId* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="3c8e0-111">*bstrArguments* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c8e0-111">*bstrArguments* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="3c8e0-112">*vbExpandEnvVarInArgumentsOnServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c8e0-112">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
<span data-ttu-id="3c8e0-113"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3c8e0-113"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="3c8e0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c8e0-114">Return value</span></span>

<span data-ttu-id="3c8e0-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3c8e0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c8e0-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3c8e0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8e0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c8e0-117">Requirements</span></span>



| <span data-ttu-id="3c8e0-118">需求</span><span class="sxs-lookup"><span data-stu-id="3c8e0-118">Requirement</span></span> | <span data-ttu-id="3c8e0-119">值</span><span class="sxs-lookup"><span data-stu-id="3c8e0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8e0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c8e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c8e0-121">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c8e0-121">Windows 10 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3c8e0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c8e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c8e0-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c8e0-123">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="3c8e0-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3c8e0-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c8e0-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c8e0-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3c8e0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3c8e0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c8e0-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c8e0-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c8e0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c8e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8e0-129">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="3c8e0-129">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> </dl>

 

 





