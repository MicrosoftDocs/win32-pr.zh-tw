---
title: system_handle 屬性
description: '\ System_handle \ 屬性指定系統定義的控制碼類型。'
keywords:
- system_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106984268"
---
# <a name="system_handle-attribute"></a><span data-ttu-id="f0263-104">system_handle 屬性</span><span class="sxs-lookup"><span data-stu-id="f0263-104">system_handle attribute</span></span>

<span data-ttu-id="f0263-105">\[ **System_handle** \] 屬性會指定代表系統物件存取權的系統定義控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="f0263-105">The \[**system_handle**\] attribute specifies a system-defined handle type that represents access to a system object.</span></span>

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a><span data-ttu-id="f0263-106">參數</span><span class="sxs-lookup"><span data-stu-id="f0263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0263-107">*系統控點類型*</span><span class="sxs-lookup"><span data-stu-id="f0263-107">*system-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f0263-108">指定其中一個系統控制碼類型選項。</span><span class="sxs-lookup"><span data-stu-id="f0263-108">Specifies one of the system handle type options.</span></span>

<span data-ttu-id="f0263-109">有效的選項為：</span><span class="sxs-lookup"><span data-stu-id="f0263-109">The valid options are:</span></span>
* <span data-ttu-id="f0263-110">[sh_composition](sh-composition.md) -DirectComposition 介面控制碼</span><span class="sxs-lookup"><span data-stu-id="f0263-110">[sh_composition](sh-composition.md) - A DirectComposition surface handle</span></span>
* <span data-ttu-id="f0263-111">[sh_event](sh-event.md) -已命名或未命名的事件物件</span><span class="sxs-lookup"><span data-stu-id="f0263-111">[sh_event](sh-event.md) - A named or unnamed event object</span></span>
* <span data-ttu-id="f0263-112">[sh_file](sh-file.md) -檔案或 i/o 裝置</span><span class="sxs-lookup"><span data-stu-id="f0263-112">[sh_file](sh-file.md) - A file or I/O device</span></span>
* <span data-ttu-id="f0263-113">[sh_job](sh-job.md) -工作物件</span><span class="sxs-lookup"><span data-stu-id="f0263-113">[sh_job](sh-job.md) - A job object</span></span>
* <span data-ttu-id="f0263-114">[sh_mutex](sh-mutex.md) -已命名或未命名的 mutex 物件</span><span class="sxs-lookup"><span data-stu-id="f0263-114">[sh_mutex](sh-mutex.md) - A named or unnamed mutex object</span></span>
* <span data-ttu-id="f0263-115">[sh_pipe](sh-pipe.md) -匿名或具名管道物件</span><span class="sxs-lookup"><span data-stu-id="f0263-115">[sh_pipe](sh-pipe.md) - An anonymous or named pipe object</span></span>
* <span data-ttu-id="f0263-116">[sh_process](sh-process.md) -進程物件</span><span class="sxs-lookup"><span data-stu-id="f0263-116">[sh_process](sh-process.md) - A process object</span></span>
* <span data-ttu-id="f0263-117">[sh_reg_key](sh-reg-key.md) -登錄機碼</span><span class="sxs-lookup"><span data-stu-id="f0263-117">[sh_reg_key](sh-reg-key.md) - A registry key</span></span>
* <span data-ttu-id="f0263-118">[sh_section](sh-section.md) -共用記憶體區段</span><span class="sxs-lookup"><span data-stu-id="f0263-118">[sh_section](sh-section.md) - A shared memory section</span></span>
* <span data-ttu-id="f0263-119">[sh_semaphore](sh-semaphore.md) -已命名或未命名的信號物件</span><span class="sxs-lookup"><span data-stu-id="f0263-119">[sh_semaphore](sh-semaphore.md) - A named or unnamed semaphore object</span></span>
* <span data-ttu-id="f0263-120">[sh_socket](sh-socket.md) -WinSock 通訊端物件</span><span class="sxs-lookup"><span data-stu-id="f0263-120">[sh_socket](sh-socket.md) - A WinSock socket object</span></span>
* <span data-ttu-id="f0263-121">[sh_thread](sh-thread.md) -執行緒物件</span><span class="sxs-lookup"><span data-stu-id="f0263-121">[sh_thread](sh-thread.md) - A thread object</span></span>
* <span data-ttu-id="f0263-122">[sh_token](sh-token.md) -存取權杖物件</span><span class="sxs-lookup"><span data-stu-id="f0263-122">[sh_token](sh-token.md) - An access token object</span></span>

</dd> <dt>

<span data-ttu-id="f0263-123">*選擇性-存取-遮罩*</span><span class="sxs-lookup"><span data-stu-id="f0263-123">*optional-access-mask*</span></span>
</dt> <dd>

<span data-ttu-id="f0263-124">選擇性地要求套用至重複控制碼的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="f0263-124">Optionally requests specific access rights applied to the duplicated handle.</span></span> <span data-ttu-id="f0263-125">依預設，當未指定時，會使用相同的存取權複製控制碼。</span><span class="sxs-lookup"><span data-stu-id="f0263-125">By default when this is unspecified, the handle will be duplicated with the same access.</span></span> 

<span data-ttu-id="f0263-126">若要指定不同層級的存取權，請使用對應于所選基礎系統物件的物件特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="f0263-126">To specify a different level of access, use object specific access rights corresponding to the underlying system object selected.</span></span>

<span data-ttu-id="f0263-127">如需有關如何在重複期間傳播存取權限的詳細資訊，請參閱 [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 檔。</span><span class="sxs-lookup"><span data-stu-id="f0263-127">More information on how access rights are propagated during duplication can be found on the [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) documentation.</span></span>

<span data-ttu-id="f0263-128">您可以在 *DuplicateHandle* 參考中找到每個物件類型的存取權限清單連結，也可以在 [ **另請參閱** 每個參數的標題] 頁面中找到 `sh_*` 。</span><span class="sxs-lookup"><span data-stu-id="f0263-128">Links to lists of access rights for each type of object can be found in the *DuplicateHandle* reference as well as in the **See also** headings of each `sh_*` parameter page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0263-129">備註</span><span class="sxs-lookup"><span data-stu-id="f0263-129">Remarks</span></span>

<span data-ttu-id="f0263-130">若要使用這個屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。</span><span class="sxs-lookup"><span data-stu-id="f0263-130">In order to use this attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

<span data-ttu-id="f0263-131">系統控制碼是作業系統所定義的控制碼，可提供系統資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="f0263-131">System handles are handles that are defined by the operating system to provide access to a system resource.</span></span> <span data-ttu-id="f0263-132">宣告屬性時，必須指定控制碼後方的特定物件類型。</span><span class="sxs-lookup"><span data-stu-id="f0263-132">The specific type of the object behind the handle must be specified when declaring the attribute.</span></span>

<span data-ttu-id="f0263-133">針對標示的控制碼 `[in]` ，此控制碼會複製到遠端程式中，並在該程式的持續時間內保持有效。</span><span class="sxs-lookup"><span data-stu-id="f0263-133">For a handle marked `[in]`, the handle will be duplicated into the remote procedure and remains valid for the duration of that procedure.</span></span> <span data-ttu-id="f0263-134">從遠端程式傳回時，會釋放重複的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f0263-134">On return from the remote procedure, the duplicated handle is freed.</span></span> <span data-ttu-id="f0263-135">為了維持對基礎物件的存取權，遠端應用程式必須將控制碼複製到它自己的位址空間中。</span><span class="sxs-lookup"><span data-stu-id="f0263-135">To maintain access to the underlying object, the remote application must duplicate the handle into its own address space.</span></span>

<span data-ttu-id="f0263-136">相反地，針對標示的控制碼， `[out]` 當遠端程式從呼叫傳回控制碼時，遠端程式將會失去其擁有權。</span><span class="sxs-lookup"><span data-stu-id="f0263-136">By contrast, for a handle marked `[out]`, when a remote procedure returns a handle from a call, the remote procedure will lose ownership of it.</span></span> <span data-ttu-id="f0263-137">為了維持對基礎物件的存取權，遠端程式應該複製控制碼，並傳回重複的。</span><span class="sxs-lookup"><span data-stu-id="f0263-137">To maintain access to the underlying object, the remote procedure should duplicate the handle and return the duplicate.</span></span> <span data-ttu-id="f0263-138">傳回的控制碼接著會由呼叫者所擁有，而該呼叫者會在不再需要基礎系統物件的存取權時，負責將其關閉。</span><span class="sxs-lookup"><span data-stu-id="f0263-138">The returned handle then becomes owned by the caller who assumes a responsibility to close it when access to the underlying system object is no longer necessary.</span></span>

<span data-ttu-id="f0263-139">因為這是轉送系統物件存取權的機制，這個屬性只適用于同一部電腦上的程式之間的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f0263-139">As this is a mechanism for relaying access to a system object, this attribute is only applicable to calls between procedures on the same machine.</span></span>

<span data-ttu-id="f0263-140">在建立及存取系統控制碼背後的基礎物件時，會決定是否可以將它成功封送處理至遠端程式內容。</span><span class="sxs-lookup"><span data-stu-id="f0263-140">The creation and access parameters given to the underlying object behind the system handle on its creation will dictate whether it can be successfully marshalled to the remote procedure context.</span></span>

<span data-ttu-id="f0263-141">的陣列 `system_handle` 可以使用 [**size_is 屬性**](size-is.md) 檔中所找到的語法，傳入或傳出。</span><span class="sxs-lookup"><span data-stu-id="f0263-141">An array of `system_handle` can be passed either in or out with the syntax found in the [**size_is attribute**](size-is.md) documentation.</span></span>

## <a name="examples"></a><span data-ttu-id="f0263-142">範例</span><span class="sxs-lookup"><span data-stu-id="f0263-142">Examples</span></span>

<span data-ttu-id="f0263-143">下列範例會使用的數個 `system_handle` 。</span><span class="sxs-lookup"><span data-stu-id="f0263-143">The following examples several uses of `system_handle`.</span></span> <span data-ttu-id="f0263-144">如需完整範例，請參閱 [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) 範例。</span><span class="sxs-lookup"><span data-stu-id="f0263-144">For a complete sample, see the [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) sample.</span></span>

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a><span data-ttu-id="f0263-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0263-145">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="f0263-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0263-146">Minimum supported client</span></span> | <span data-ttu-id="f0263-147">Windows 10 年度更新版 (1607 版、組建 14393) </span><span class="sxs-lookup"><span data-stu-id="f0263-147">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="f0263-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0263-148">Minimum supported server</span></span> | <span data-ttu-id="f0263-149">Windows Server 2016 (build 14393) </span><span class="sxs-lookup"><span data-stu-id="f0263-149">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f0263-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0263-150">See also</span></span>

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[<span data-ttu-id="f0263-151">/target 參數</span><span class="sxs-lookup"><span data-stu-id="f0263-151">/target switch</span></span>](./-target.md)
</dt> <dt>

[<span data-ttu-id="f0263-152">系結和控制碼</span><span class="sxs-lookup"><span data-stu-id="f0263-152">Binding and Handles</span></span>](../Rpc/binding-and-handles.md)
</dt> <dt>

[<span data-ttu-id="f0263-153">控制碼和物件</span><span class="sxs-lookup"><span data-stu-id="f0263-153">Handles and Objects</span></span>](../sysinfo/handles-and-objects.md)
</dt> <dt>

[<span data-ttu-id="f0263-154"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="f0263-154">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f0263-155">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="f0263-155">**DuplicateHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="f0263-156">安全性描述項</span><span class="sxs-lookup"><span data-stu-id="f0263-156">Security Descriptors</span></span>](../secauthz/security-descriptors.md)
</dt></dl>
