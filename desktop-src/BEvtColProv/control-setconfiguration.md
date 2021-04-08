---
description: 設定收集器的新使用中設定。
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Control 類別的 SetConfiguration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688568"
---
# <a name="setconfiguration-method-of-the-control-class"></a><span data-ttu-id="a4888-103">Control 類別的 SetConfiguration 方法</span><span class="sxs-lookup"><span data-stu-id="a4888-103">SetConfiguration method of the Control class</span></span>

<span data-ttu-id="a4888-104">設定收集器的新使用中設定。</span><span class="sxs-lookup"><span data-stu-id="a4888-104">Set the new active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4888-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4888-105">Syntax</span></span>


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="a4888-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4888-107">*Config* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4888-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-108">要啟動的設定。</span><span class="sxs-lookup"><span data-stu-id="a4888-108">The configuration to activate.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-109">*OldTimestampLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4888-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-110">時間戳記的低序位位，指出目前使用中的設定是否已設定。</span><span class="sxs-lookup"><span data-stu-id="a4888-110">The low-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="a4888-111">如果這個屬性未設定為0，則會啟用不可部分完成性檢查。</span><span class="sxs-lookup"><span data-stu-id="a4888-111">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-112">*OldTimestampHigh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4888-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-113">時間戳記的高序位位，指出目前使用中的設定是否已設定。</span><span class="sxs-lookup"><span data-stu-id="a4888-113">The high-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="a4888-114">如果這個屬性未設定為0，則會啟用不可部分完成性檢查。</span><span class="sxs-lookup"><span data-stu-id="a4888-114">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-115">*NewTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4888-115">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-116">當此方法傳回時，此參數會包含時間戳記的低序位位，指出設定新設定的時間。</span><span class="sxs-lookup"><span data-stu-id="a4888-116">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="a4888-117">如果這個屬性未設定為0，則會啟用不可部分完成性檢查。</span><span class="sxs-lookup"><span data-stu-id="a4888-117">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-118">*NewTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4888-118">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-119">當此方法傳回時，此參數會包含時間戳記的高序位位，指出設定新設定的時間。</span><span class="sxs-lookup"><span data-stu-id="a4888-119">When this method returns, this parameter contains the high-order bits of the timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="a4888-120">如果這個屬性未設定為0，則會啟用不可部分完成性檢查。</span><span class="sxs-lookup"><span data-stu-id="a4888-120">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-121">*ErrorString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4888-121">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-122">當此方法傳回時，如果發生錯誤，此參數就會包含錯誤描述。</span><span class="sxs-lookup"><span data-stu-id="a4888-122">When this method returns, if there was an error, this parameter contains the error description.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-123">*WarningString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4888-123">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-124">當此方法傳回時，此參數會包含任何作業的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="a4888-124">When this method returns, this parameter contains any warnings messages for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-125">*InfoString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4888-125">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-126">當此方法傳回時，此參數會包含新的使用中設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="a4888-126">When this method returns, this parameter contains information for the new active configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-127">*ErrorType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4888-127">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4888-128">當此方法傳回時，如果發生錯誤，此參數會指出錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="a4888-128">When this method returns, if there was an error, this parameter indicates the error type.</span></span>

<dt>

<span data-ttu-id="a4888-129">0</span><span class="sxs-lookup"><span data-stu-id="a4888-129">0</span></span>
</dt> <dd>

<span data-ttu-id="a4888-130">缺少新的設定。</span><span class="sxs-lookup"><span data-stu-id="a4888-130">The new configuration is missing.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-131">1</span><span class="sxs-lookup"><span data-stu-id="a4888-131">1</span></span>
</dt> <dd>

<span data-ttu-id="a4888-132">新設定的格式無效。</span><span class="sxs-lookup"><span data-stu-id="a4888-132">The format of the new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-133">2</span><span class="sxs-lookup"><span data-stu-id="a4888-133">2</span></span>
</dt> <dd>

<span data-ttu-id="a4888-134">新的設定無效。</span><span class="sxs-lookup"><span data-stu-id="a4888-134">The new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-135">3</span><span class="sxs-lookup"><span data-stu-id="a4888-135">3</span></span>
</dt> <dd>

<span data-ttu-id="a4888-136">開啟的通訊端造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4888-136">There was an error caused by an open socket.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-137">4</span><span class="sxs-lookup"><span data-stu-id="a4888-137">4</span></span>
</dt> <dd>

<span data-ttu-id="a4888-138">發生檔案寫入錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4888-138">There was a file write error.</span></span>

</dd> <dt>

<span data-ttu-id="a4888-139">5</span><span class="sxs-lookup"><span data-stu-id="a4888-139">5</span></span>
</dt> <dd>

<span data-ttu-id="a4888-140">發生不可部分完成性錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4888-140">There was an atomicity error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4888-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4888-141">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a4888-142">0</span><span class="sxs-lookup"><span data-stu-id="a4888-142">0</span></span>

<span data-ttu-id="a4888-143">失敗</span><span class="sxs-lookup"><span data-stu-id="a4888-143">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a4888-144">1</span><span class="sxs-lookup"><span data-stu-id="a4888-144">1</span></span>

<span data-ttu-id="a4888-145">Success</span><span class="sxs-lookup"><span data-stu-id="a4888-145">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4888-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4888-146">Requirements</span></span>



| <span data-ttu-id="a4888-147">需求</span><span class="sxs-lookup"><span data-stu-id="a4888-147">Requirement</span></span> | <span data-ttu-id="a4888-148">值</span><span class="sxs-lookup"><span data-stu-id="a4888-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4888-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4888-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a4888-150">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4888-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a4888-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4888-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a4888-152">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a4888-152">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="a4888-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4888-153">Namespace</span></span><br/>                | <span data-ttu-id="a4888-154">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="a4888-154">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="a4888-155">MOF</span><span class="sxs-lookup"><span data-stu-id="a4888-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4888-156"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4888-156"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4888-157">DLL</span><span class="sxs-lookup"><span data-stu-id="a4888-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4888-158"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4888-158"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a4888-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4888-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4888-160">**控制**</span><span class="sxs-lookup"><span data-stu-id="a4888-160">**Control**</span></span>](control.md)
</dt> </dl>

 

 




