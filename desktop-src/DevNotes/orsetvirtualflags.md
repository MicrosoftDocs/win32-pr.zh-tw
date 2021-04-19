---
description: 在離線登錄區中，于指定的開啟登錄機碼上設定虛擬旗標。
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: 'ORSetVirtualFlags 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: f694d69684a474cfa6d4f6c33c6d8cab7072f605
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988253"
---
# <a name="orsetvirtualflags-function"></a><span data-ttu-id="03178-103">ORSetVirtualFlags 函式</span><span class="sxs-lookup"><span data-stu-id="03178-103">ORSetVirtualFlags function</span></span>

<span data-ttu-id="03178-104">在離線登錄區中，于指定的開啟登錄機碼上設定虛擬旗標。</span><span class="sxs-lookup"><span data-stu-id="03178-104">Sets virtualization flags on the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="03178-105">語法</span><span class="sxs-lookup"><span data-stu-id="03178-105">Syntax</span></span>


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="03178-106">參數</span><span class="sxs-lookup"><span data-stu-id="03178-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03178-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03178-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03178-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03178-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="03178-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03178-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03178-110">此參數會控制在虛擬化 hive 中的索引鍵上建立或開啟作業失敗時的登錄行為。</span><span class="sxs-lookup"><span data-stu-id="03178-110">This parameter controls the behavior of the registry when a Create or Open operation fails on a key in a virtualized hive.</span></span> <span data-ttu-id="03178-111">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="03178-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="03178-112">值</span><span class="sxs-lookup"><span data-stu-id="03178-112">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="03178-113">意義</span><span class="sxs-lookup"><span data-stu-id="03178-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <span data-ttu-id="03178-114"><dt>**REG \_機碼不是 \_ \_ 無訊息 \_ 失敗**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="03178-114"><dt>**REG\_KEY\_DONT\_SILENT\_FAIL**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="03178-115">如果設定此旗標，且已啟用虛擬化的金鑰上的開啟操作失敗，則登錄不會嘗試重新開啟金鑰。</span><span class="sxs-lookup"><span data-stu-id="03178-115">If this flag is set and an Open operation fails on a key for which virtualization is enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="03178-116">如果清除此旗標，登錄會嘗試以允許的最大存取權重新開啟金鑰 \_ 。</span><span class="sxs-lookup"><span data-stu-id="03178-116">If this flag is clear, the registry attempts to reopen the key with the MAXIMUM\_ALLOWED access.</span></span><br/>                                                                                    |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <span data-ttu-id="03178-117"><dt>**REG \_機碼不會 \_ \_ 虛擬化**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="03178-117"><dt>**REG\_KEY\_DONT\_VIRTUALIZE**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="03178-118">如果設定此旗標，且建立索引鍵作業失敗，因為呼叫端沒有父索引鍵的 KEY \_ Create \_ SUB \_ key，則登錄會使建立作業失敗。</span><span class="sxs-lookup"><span data-stu-id="03178-118">If this flag is set and a Create Key operation fails because the caller does not have the KEY\_CREATE\_SUB\_KEY right on the parent key, the registry fails the Create operation.</span></span> <span data-ttu-id="03178-119">如果清除此旗標，登錄會嘗試在虛擬存放區中建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="03178-119">If this flag is clear, the registry attempts to create the key in the virtual store.</span></span> <span data-ttu-id="03178-120">呼叫 \_ 端必須在父機碼上具有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="03178-120">The caller must have the KEY\_READ right on the parent key.</span></span><br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <span data-ttu-id="03178-121"><dt>**REG \_按鍵 \_ 遞迴 \_ 旗**</dt>標 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="03178-121"><dt>**REG\_KEY\_RECURSE\_FLAG**</dt> <dt>8</dt></span></span> </dl>              | <span data-ttu-id="03178-122">如果設定此旗標，則會從父機碼傳播登錄虛擬旗標。</span><span class="sxs-lookup"><span data-stu-id="03178-122">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="03178-123">如果清除此旗標，則不會傳播登錄虛擬旗標。</span><span class="sxs-lookup"><span data-stu-id="03178-123">If this flag is clear, registry virtualization flags are not propagated.</span></span><br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03178-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="03178-124">Return value</span></span>

<span data-ttu-id="03178-125">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="03178-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="03178-126">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="03178-126">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="03178-127">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="03178-127">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="03178-128">備註</span><span class="sxs-lookup"><span data-stu-id="03178-128">Remarks</span></span>

<span data-ttu-id="03178-129">登錄虛擬化是一項過渡的應用程式相容性技術，可讓具有全域影響的登錄寫入作業重新導向至每個使用者的位置。</span><span class="sxs-lookup"><span data-stu-id="03178-129">Registry virtualization is an interim application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="03178-130">對於讀取或寫入登錄的應用程式而言，此重新導向是透明的。</span><span class="sxs-lookup"><span data-stu-id="03178-130">This redirection is transparent to applications reading from or writing to the registry.</span></span>

<span data-ttu-id="03178-131">從 Windows Vista 開始支援登錄虛擬化。</span><span class="sxs-lookup"><span data-stu-id="03178-131">Registry virtualization is supported starting with Windows Vista.</span></span> <span data-ttu-id="03178-132">不過，Microsoft 打算將它從未來版本的 Windows 作業系統中移除，因為更多應用程式都與 Windows Vista 相容。</span><span class="sxs-lookup"><span data-stu-id="03178-132">However, Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista.</span></span> <span data-ttu-id="03178-133">因此，應用程式不應該依賴系統中的登錄虛擬化行為。</span><span class="sxs-lookup"><span data-stu-id="03178-133">Therefore, applications should not depend on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="03178-134">登錄虛擬化只會針對下列各項啟用：</span><span class="sxs-lookup"><span data-stu-id="03178-134">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="03178-135">32位互動式進程</span><span class="sxs-lookup"><span data-stu-id="03178-135">32-bit interactive processes</span></span>
-   <span data-ttu-id="03178-136">**HKEY \_ 本機 \_ 電腦 \\ 軟體** 中的金鑰</span><span class="sxs-lookup"><span data-stu-id="03178-136">Keys in **HKEY\_LOCAL\_MACHINE\\Software**</span></span>
-   <span data-ttu-id="03178-137">系統管理員可寫入的金鑰</span><span class="sxs-lookup"><span data-stu-id="03178-137">Keys that an administrator can write to</span></span>

<span data-ttu-id="03178-138">如需詳細資訊，請參閱登錄 [虛擬化](../sysinfo/registry-virtualization.md)。</span><span class="sxs-lookup"><span data-stu-id="03178-138">For more information, see [Registry Virtualization](../sysinfo/registry-virtualization.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03178-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="03178-139">Requirements</span></span>



| <span data-ttu-id="03178-140">需求</span><span class="sxs-lookup"><span data-stu-id="03178-140">Requirement</span></span> | <span data-ttu-id="03178-141">值</span><span class="sxs-lookup"><span data-stu-id="03178-141">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03178-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="03178-142">Redistributable</span></span><br/> | <span data-ttu-id="03178-143">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="03178-143">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="03178-144">標頭</span><span class="sxs-lookup"><span data-stu-id="03178-144">Header</span></span><br/>          | <dl> <span data-ttu-id="03178-145"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="03178-145"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="03178-146">DLL</span><span class="sxs-lookup"><span data-stu-id="03178-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="03178-147"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03178-147"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03178-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03178-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03178-149">**ORGetVirtualFlags**</span><span class="sxs-lookup"><span data-stu-id="03178-149">**ORGetVirtualFlags**</span></span>](orgetvirtualflags.md)
</dt> <dt>

[<span data-ttu-id="03178-150">登錄虛擬化</span><span class="sxs-lookup"><span data-stu-id="03178-150">Registry Virtualization</span></span>](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
