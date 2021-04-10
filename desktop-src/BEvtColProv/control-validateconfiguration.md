---
description: 驗證設定文字的正確性，而不將其設定為使用中。 在成功時傳回1，錯誤則為0。
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Control 類別的 ValidateConfiguration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936065"
---
# <a name="validateconfiguration-method-of-the-control-class"></a><span data-ttu-id="07288-104">Control 類別的 ValidateConfiguration 方法</span><span class="sxs-lookup"><span data-stu-id="07288-104">ValidateConfiguration method of the Control class</span></span>

<span data-ttu-id="07288-105">驗證設定文字的正確性，而不將其設定為使用中。</span><span class="sxs-lookup"><span data-stu-id="07288-105">Validate a configuration text for correctness without setting it active.</span></span> <span data-ttu-id="07288-106">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="07288-106">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="07288-107">語法</span><span class="sxs-lookup"><span data-stu-id="07288-107">Syntax</span></span>


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="07288-108">參數</span><span class="sxs-lookup"><span data-stu-id="07288-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07288-109">*Config* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07288-109">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07288-110">要檢查的設定。</span><span class="sxs-lookup"><span data-stu-id="07288-110">The configuration to check.</span></span>

</dd> <dt>

<span data-ttu-id="07288-111">*ErrorString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07288-111">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07288-112">當此方法傳回時，如果發生錯誤，此參數會包含作業之驗證錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="07288-112">When this method returns, if there was a error, this parameter contains a description of the validation error for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="07288-113">*WarningString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07288-113">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07288-114">當此方法傳回時，此參數會包含作業之任何驗證警告的描述。</span><span class="sxs-lookup"><span data-stu-id="07288-114">When this method returns, this parameter contains a description of any validation warnings for the operation.</span></span>

<span data-ttu-id="07288-115">具有警告的文字字串。</span><span class="sxs-lookup"><span data-stu-id="07288-115">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="07288-116">*InfoString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07288-116">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07288-117">當此方法傳回時，此參數會包含一組有關設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="07288-117">When this method returns, this parameter contains a set of information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="07288-118">*ErrorType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07288-118">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07288-119">當此方法傳回時，如果發生驗證錯誤，此參數會指出錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="07288-119">When this method returns, if there was a validation error, this parameter indicates the error type.</span></span>

<span data-ttu-id="07288-120">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="07288-120">The possible values are:</span></span>

<dt>

<span data-ttu-id="07288-121">0</span><span class="sxs-lookup"><span data-stu-id="07288-121">0</span></span>
</dt> <dd>

<span data-ttu-id="07288-122">遺漏引數。</span><span class="sxs-lookup"><span data-stu-id="07288-122">The argument is missing.</span></span>

</dd> <dt>

<span data-ttu-id="07288-123">1</span><span class="sxs-lookup"><span data-stu-id="07288-123">1</span></span>
</dt> <dd>

<span data-ttu-id="07288-124">引數格式無效。</span><span class="sxs-lookup"><span data-stu-id="07288-124">The argument format is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="07288-125">2</span><span class="sxs-lookup"><span data-stu-id="07288-125">2</span></span>
</dt> <dd>

<span data-ttu-id="07288-126">設定引數無效。</span><span class="sxs-lookup"><span data-stu-id="07288-126">A configuration argument is invalid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07288-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="07288-127">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="07288-128">0</span><span class="sxs-lookup"><span data-stu-id="07288-128">0</span></span>

<span data-ttu-id="07288-129">失敗</span><span class="sxs-lookup"><span data-stu-id="07288-129">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07288-130">1</span><span class="sxs-lookup"><span data-stu-id="07288-130">1</span></span>

<span data-ttu-id="07288-131">Success</span><span class="sxs-lookup"><span data-stu-id="07288-131">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07288-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="07288-132">Requirements</span></span>



| <span data-ttu-id="07288-133">需求</span><span class="sxs-lookup"><span data-stu-id="07288-133">Requirement</span></span> | <span data-ttu-id="07288-134">值</span><span class="sxs-lookup"><span data-stu-id="07288-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07288-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07288-135">Minimum supported client</span></span><br/> | <span data-ttu-id="07288-136">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07288-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="07288-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07288-137">Minimum supported server</span></span><br/> | <span data-ttu-id="07288-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="07288-138">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="07288-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="07288-139">Namespace</span></span><br/>                | <span data-ttu-id="07288-140">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="07288-140">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="07288-141">MOF</span><span class="sxs-lookup"><span data-stu-id="07288-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07288-142"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="07288-142"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="07288-143">DLL</span><span class="sxs-lookup"><span data-stu-id="07288-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07288-144"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="07288-144"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="07288-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07288-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07288-146">**控制**</span><span class="sxs-lookup"><span data-stu-id="07288-146">**Control**</span></span>](control.md)
</dt> </dl>

 

 




