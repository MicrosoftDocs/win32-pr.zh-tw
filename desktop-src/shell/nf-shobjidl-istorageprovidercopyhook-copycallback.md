---
description: 決定是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104991842"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a><span data-ttu-id="5ee57-103">IStorageProviderCopyHook：： CopyCallback 方法</span><span class="sxs-lookup"><span data-stu-id="5ee57-103">IStorageProviderCopyHook::CopyCallback method</span></span>

<span data-ttu-id="5ee57-104">決定是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5ee57-104">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee57-105">語法</span><span class="sxs-lookup"><span data-stu-id="5ee57-105">Syntax</span></span>

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a><span data-ttu-id="5ee57-106">參數</span><span class="sxs-lookup"><span data-stu-id="5ee57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ee57-107">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ee57-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee57-108">針對處理常式可能需要顯示之任何使用者介面元素的父代，複製攔截處理常式應該使用的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="5ee57-108">A handle to the window that the copy hook handler should use as the parent for any user interface elements the handler may need to display.</span></span> <span data-ttu-id="5ee57-109">如果在 *作業中指定* **FOF_SILENT** ，則方法應忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="5ee57-109">If **FOF_SILENT** is specified in *operation*, the method should ignore this parameter.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5ee57-110">*操作* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ee57-110">*operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee57-111">要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="5ee57-111">The operation to perform.</span></span> <span data-ttu-id="5ee57-112">這個參數可以是 [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa)結構的 **wFunc** 成員下所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5ee57-112">This parameter can be one of the values listed under the **wFunc** member of the [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5ee57-113">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ee57-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee57-114">控制作業的旗標。</span><span class="sxs-lookup"><span data-stu-id="5ee57-114">The flags that control the operation.</span></span> <span data-ttu-id="5ee57-115">這個參數可以是 [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa)結構的 *fFlags* 成員下所列的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="5ee57-115">This parameter can be one or more of the values listed under the *fFlags* member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

<span data-ttu-id="5ee57-116">若是印表機複製勾點，此值是在 shellapi 中定義的下列值之一。</span><span class="sxs-lookup"><span data-stu-id="5ee57-116">For printer copy hooks, this value is one of the following values defined in shellapi.h.</span></span>

| <span data-ttu-id="5ee57-117">值</span><span class="sxs-lookup"><span data-stu-id="5ee57-117">Value</span></span>       | <span data-ttu-id="5ee57-118">描述</span><span class="sxs-lookup"><span data-stu-id="5ee57-118">Description</span></span> |
|-------------|------------|
|  <span data-ttu-id="5ee57-119">**PO_DELETE**</span><span class="sxs-lookup"><span data-stu-id="5ee57-119">**PO_DELETE**</span></span>      | <span data-ttu-id="5ee57-120">正在刪除印表機。</span><span class="sxs-lookup"><span data-stu-id="5ee57-120">A printer is being deleted.</span></span> <span data-ttu-id="5ee57-121">*SrcFile* 參數指向指定印表機的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5ee57-121">The *srcFile* parameter points to the full path to the specified printer.</span></span>           |
|  <span data-ttu-id="5ee57-122">**PO_RENAME**</span><span class="sxs-lookup"><span data-stu-id="5ee57-122">**PO_RENAME**</span></span>       | <span data-ttu-id="5ee57-123">印表機已重新命名。</span><span class="sxs-lookup"><span data-stu-id="5ee57-123">A printer is being renamed.</span></span> <span data-ttu-id="5ee57-124">*SrcFile* 參數會指向印表機的新名稱。</span><span class="sxs-lookup"><span data-stu-id="5ee57-124">The *srcFile* parameter points to the printer's new name.</span></span> <span data-ttu-id="5ee57-125">*DestFile* 參數會指向舊的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ee57-125">The *destFile* parameter points to the old name.</span></span>           |
| <span data-ttu-id="5ee57-126">**PO_PORTCHANGE**</span><span class="sxs-lookup"><span data-stu-id="5ee57-126">**PO_PORTCHANGE**</span></span>    | <span data-ttu-id="5ee57-127">不支援。</span><span class="sxs-lookup"><span data-stu-id="5ee57-127">Not supported.</span></span> <span data-ttu-id="5ee57-128">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="5ee57-128">Do not use.</span></span>          |
| <span data-ttu-id="5ee57-129">**PO_REN_PORT**</span><span class="sxs-lookup"><span data-stu-id="5ee57-129">**PO_REN_PORT**</span></span>    | <span data-ttu-id="5ee57-130">不支援。</span><span class="sxs-lookup"><span data-stu-id="5ee57-130">Not supported.</span></span> <span data-ttu-id="5ee57-131">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="5ee57-131">Do not use.</span></span>           |

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5ee57-132">*srcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ee57-132">*srcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee57-133">包含源資料夾名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="5ee57-133">A pointer to a string that contains the name of the source folder.</span></span>

</dd> </dl>

<span data-ttu-id="5ee57-134">*srcAttribs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ee57-134">*srcAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee57-135">源資料夾的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ee57-135">The attributes of the source folder.</span></span> <span data-ttu-id="5ee57-136">這個參數可以是標頭檔中所定義之任何檔案屬性旗標 (FILE_ATTRIBUTE_ \* ) 的組合。</span><span class="sxs-lookup"><span data-stu-id="5ee57-136">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="5ee57-137">請參閱 [檔案屬性常數](../fileio/file-attribute-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="5ee57-137">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="5ee57-138">*destFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ee57-138">*destFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee57-139">包含目的資料夾名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="5ee57-139">A pointer to a string that contains the name of the destination folder.</span></span>

</dd> </dl>

<span data-ttu-id="5ee57-140">*destAttribs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ee57-140">*destAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee57-141">目的資料夾的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ee57-141">The attributes of the destination folder.</span></span> <span data-ttu-id="5ee57-142">這個參數可以是標頭檔中所定義之任何檔案屬性旗標 (FILE_ATTRIBUTE_ \* ) 的組合。</span><span class="sxs-lookup"><span data-stu-id="5ee57-142">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="5ee57-143">請參閱 [檔案屬性常數](../fileio/file-attribute-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="5ee57-143">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="5ee57-144">*結果* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5ee57-144">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee57-145">整數值，指出 Shell 是否應執行作業。</span><span class="sxs-lookup"><span data-stu-id="5ee57-145">The integer value that indicates whether the Shell should perform the operation.</span></span> <span data-ttu-id="5ee57-146">下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="5ee57-146">One of the following:</span></span>

| <span data-ttu-id="5ee57-147">值</span><span class="sxs-lookup"><span data-stu-id="5ee57-147">Value</span></span>       | <span data-ttu-id="5ee57-148">描述</span><span class="sxs-lookup"><span data-stu-id="5ee57-148">Description</span></span> |
|-------------|------------|
| <span data-ttu-id="5ee57-149">**IDYES**</span><span class="sxs-lookup"><span data-stu-id="5ee57-149">**IDYES**</span></span>       | <span data-ttu-id="5ee57-150">允許操作。</span><span class="sxs-lookup"><span data-stu-id="5ee57-150">Allows the operation.</span></span>           |
| <span data-ttu-id="5ee57-151">**IDNO**</span><span class="sxs-lookup"><span data-stu-id="5ee57-151">**IDNO**</span></span>        | <span data-ttu-id="5ee57-152">防止此資料夾上的作業，但會繼續進行已核准 (例如，批次複製作業) 的任何其他作業。</span><span class="sxs-lookup"><span data-stu-id="5ee57-152">Prevents the operation on this folder but continues with any other operations that have been approved (for example, a batch copy operation).</span></span>           |
| <span data-ttu-id="5ee57-153">**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="5ee57-153">**IDCANCEL**</span></span>    | <span data-ttu-id="5ee57-154">防止目前的作業，並取消任何暫止的作業。</span><span class="sxs-lookup"><span data-stu-id="5ee57-154">Prevents the current operation and cancels any pending operations.</span></span>           |


</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="5ee57-155">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ee57-155">Return value</span></span>

<span data-ttu-id="5ee57-156">如果成功，則傳回 **S_OK** ，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5ee57-156">Returns **S_OK** if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ee57-157">備註</span><span class="sxs-lookup"><span data-stu-id="5ee57-157">Remarks</span></span>

<span data-ttu-id="5ee57-158">Shell 會針對註冊的同步根目錄下的每個資料夾，呼叫雲端提供者的複製勾點處理常式。</span><span class="sxs-lookup"><span data-stu-id="5ee57-158">The Shell calls the cloud provider's copy hook handler for every folder under the registered sync root.</span></span> <span data-ttu-id="5ee57-159">若要註冊雲端資料夾的複製勾點處理常式，請將 **HKEY_LOCAL_MACHINE/software/microsoft/windows/currentversion/explorer/syncrootmanager/{syncrootid}** 機碼底下的 **CopyHook** 值設定為複製攔截物件的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="5ee57-159">To register a copy hook handler for cloud folders, set the **CopyHook** value under the **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** key to the CLSID of the copy hook object.</span></span>

<span data-ttu-id="5ee57-160">呼叫 **CopyCallback** 方法時，Shell 會直接初始化 [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) 介面，而不會先使用 [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面。</span><span class="sxs-lookup"><span data-stu-id="5ee57-160">When the **CopyCallback** method is called, the Shell initializes the [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) interface directly without using an [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee57-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ee57-161">Requirements</span></span>

| <span data-ttu-id="5ee57-162">需求</span><span class="sxs-lookup"><span data-stu-id="5ee57-162">Requirement</span></span> | <span data-ttu-id="5ee57-163">值</span><span class="sxs-lookup"><span data-stu-id="5ee57-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee57-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ee57-164">Minimum supported client</span></span> | <span data-ttu-id="5ee57-165">Windows 10 Insider Preview 組建19624</span><span class="sxs-lookup"><span data-stu-id="5ee57-165">Windows 10 Insider Preview Build 19624</span></span>                                |
| <span data-ttu-id="5ee57-166">標頭</span><span class="sxs-lookup"><span data-stu-id="5ee57-166">Header</span></span>                   | <span data-ttu-id="5ee57-167">shobjidl.h。h</span><span class="sxs-lookup"><span data-stu-id="5ee57-167">shobjidl.h</span></span>   |

## <a name="see-also"></a><span data-ttu-id="5ee57-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ee57-168">See also</span></span>

[<span data-ttu-id="5ee57-169">建立支援預留位置檔案的雲端同步處理引擎</span><span class="sxs-lookup"><span data-stu-id="5ee57-169">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](../cfapi/build-a-cloud-file-sync-engine.md)