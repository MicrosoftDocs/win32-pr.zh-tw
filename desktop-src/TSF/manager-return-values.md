---
title: '管理員傳回值 (Msctf .h) '
description: 文字服務架構會從0xHHHH0200 到0xHHHH0507 的範圍內產生傳回值。 下表提供管理員以字母順序排列的值。
ms.assetid: 12178252-c246-4fa4-bf7b-2445b859ec01
topic_type:
- apiref
api_name:
- Manager Return Values
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea9c813f9ba71371f45e2475f73af4f3016e17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509139"
---
# <a name="manager-return-values"></a><span data-ttu-id="1f415-104">管理員傳回值</span><span class="sxs-lookup"><span data-stu-id="1f415-104">Manager Return Values</span></span>

<span data-ttu-id="1f415-105">文字服務架構會從 0x *hhhh hhhh* 0200 到 0x *hhhh hhhh* 0507 的範圍產生傳回值。</span><span class="sxs-lookup"><span data-stu-id="1f415-105">The Text Services Framework produces return values in the range from 0x *HHHH* 0200 through 0x *HHHH* 0507.</span></span> <span data-ttu-id="1f415-106">下表提供管理員以字母順序排列的值。</span><span class="sxs-lookup"><span data-stu-id="1f415-106">The following table gives the manager return values in alphabetical order.</span></span>

> [!Note]  
> <span data-ttu-id="1f415-107">提供的描述不是特定的;傳回值的意義會根據傳回值的方法而不同。</span><span class="sxs-lookup"><span data-stu-id="1f415-107">The descriptions supplied are non-specific; the meaning of a return value can vary depending on the method that returned the value.</span></span>

 



| <span data-ttu-id="1f415-108">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1f415-108">Return code/value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="1f415-109">Description</span><span class="sxs-lookup"><span data-stu-id="1f415-109">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="TF_E_ALREADY_EXISTS"></span><span id="tf_e_already_exists"></span><dl> <span data-ttu-id="1f415-110"><dt>**TF \_E \_ 已經 \_ 存在**</dt> <dt>0x80040506</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-110"><dt>**TF\_E\_ALREADY\_EXISTS**</dt> <dt>0x80040506</dt></span></span> </dl>                   | <span data-ttu-id="1f415-111">已註冊保留的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1f415-111">The preserved key is registered.</span></span><br/>                                                       |
| <span id="TF_E_COMPOSITION_REJECTED"></span><span id="tf_e_composition_rejected"></span><dl> <span data-ttu-id="1f415-112"><dt>**TF \_E \_ 組合已 \_ 拒絕**</dt> <dt>0x80040508</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-112"><dt>**TF\_E\_COMPOSITION\_REJECTED**</dt> <dt>0x80040508</dt></span></span> </dl> | <span data-ttu-id="1f415-113">內容擁有者拒絕撰寫。</span><span class="sxs-lookup"><span data-stu-id="1f415-113">The context owner rejected the composition.</span></span><br/>                                            |
| <span id="TF_E_DISCONNECTED"></span><span id="tf_e_disconnected"></span><dl> <span data-ttu-id="1f415-114"><dt>**TF \_E \_ 中斷**</dt>連線 <dt>0x80040504</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-114"><dt>**TF\_E\_DISCONNECTED**</dt> <dt>0x80040504</dt></span></span> </dl>                          | <span data-ttu-id="1f415-115">內容物件不在檔堆疊上。</span><span class="sxs-lookup"><span data-stu-id="1f415-115">The context object is not on a document stack.</span></span><br/>                                         |
| <span id="TF_E_EMPTYCONTEXT"></span><span id="tf_e_emptycontext"></span><dl> <span data-ttu-id="1f415-116"><dt>**TF \_E \_ EMPTYCONTEXT**</dt> <dt>0x80040509</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-116"><dt>**TF\_E\_EMPTYCONTEXT**</dt> <dt>0x80040509</dt></span></span> </dl>                          | <span data-ttu-id="1f415-117">內容是空的。</span><span class="sxs-lookup"><span data-stu-id="1f415-117">The context is empty.</span></span><br/>                                                                  |
| <span id="TF_E_FORMAT"></span><span id="tf_e_format"></span><dl> <span data-ttu-id="1f415-118"><dt>**TF \_E \_ FORMAT**</dt> <dt>0x8004020a</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-118"><dt>**TF\_E\_FORMAT**</dt> <dt>0x8004020a</dt></span></span> </dl>                                            | <span data-ttu-id="1f415-119">內容擁有者無法處理 pDataObject 參數所提供之類型的物件。</span><span class="sxs-lookup"><span data-stu-id="1f415-119">Context owner cannot handle objects of the type provided by the pDataObject parameter.</span></span><br/> |
| <span id="TF_E_INVALIDPOINT"></span><span id="tf_e_invalidpoint"></span><dl> <span data-ttu-id="1f415-120"><dt>**TF \_E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-120"><dt>**TF\_E\_INVALIDPOINT**</dt> <dt>0x80040207</dt></span></span> </dl>                          | <span data-ttu-id="1f415-121">螢幕座標無效。</span><span class="sxs-lookup"><span data-stu-id="1f415-121">The screen coordinates are invalid.</span></span><br/>                                                    |
| <span id="TF_E_INVALIDPOS"></span><span id="tf_e_invalidpos"></span><dl> <span data-ttu-id="1f415-122"><dt>**TF \_E \_ INVALIDPOS**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-122"><dt>**TF\_E\_INVALIDPOS**</dt> <dt>0x80040200</dt></span></span> </dl>                                | <span data-ttu-id="1f415-123">字元位置無效。</span><span class="sxs-lookup"><span data-stu-id="1f415-123">The character position is invalid.</span></span><br/>                                                     |
| <span id="TF_E_INVALIDVIEW"></span><span id="tf_e_invalidview"></span><dl> <span data-ttu-id="1f415-124"><dt>**TF \_E \_ INVALIDVIEW**</dt> <dt>0x80040505</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-124"><dt>**TF\_E\_INVALIDVIEW**</dt> <dt>0x80040505</dt></span></span> </dl>                             | <span data-ttu-id="1f415-125">內容視圖無效。</span><span class="sxs-lookup"><span data-stu-id="1f415-125">The context view is invalid.</span></span><br/>                                                           |
| <span id="TF_E_LOCKED"></span><span id="tf_e_locked"></span><dl> <span data-ttu-id="1f415-126"><dt>**TF \_E \_ 鎖定**</dt>的 <dt>0x80040500</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-126"><dt>**TF\_E\_LOCKED**</dt> <dt>0x80040500</dt></span></span> </dl>                                            | <span data-ttu-id="1f415-127">已經鎖定內容。</span><span class="sxs-lookup"><span data-stu-id="1f415-127">The context is already locked.</span></span><br/>                                                         |
| <span id="TF_E_NOINTERFACE"></span><span id="tf_e_nointerface"></span><dl> <span data-ttu-id="1f415-128"><dt>**TF \_E \_ NOINTERFACE**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-128"><dt>**TF\_E\_NOINTERFACE**</dt> <dt>0x80040204</dt></span></span> </dl>                             | <span data-ttu-id="1f415-129">物件不支援要求的介面。</span><span class="sxs-lookup"><span data-stu-id="1f415-129">The object does not support the requested interface.</span></span><br/>                                   |
| <span id="TF_E_NOLAYOUT"></span><span id="tf_e_nolayout"></span><dl> <span data-ttu-id="1f415-130"><dt>**TF \_E \_ NOLAYOUT**</dt> <dt>0x80040206</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-130"><dt>**TF\_E\_NOLAYOUT**</dt> <dt>0x80040206</dt></span></span> </dl>                                      | <span data-ttu-id="1f415-131">尚未計算文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="1f415-131">The text layout has not been calculated.</span></span><br/>                                               |
| <span id="TF_E_NOLOCK"></span><span id="tf_e_nolock"></span><dl> <span data-ttu-id="1f415-132"><dt>**TF \_E \_ NOLOCK**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-132"><dt>**TF\_E\_NOLOCK**</dt> <dt>0x80040201</dt></span></span> </dl>                                            | <span data-ttu-id="1f415-133">呼叫端沒有所需的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="1f415-133">The caller does not have the necessary type of document.</span></span><br/>                               |
| <span id="TF_E_NOOBJECT"></span><span id="tf_e_noobject"></span><dl> <span data-ttu-id="1f415-134"><dt>**TF \_E \_ NOOBJECT**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-134"><dt>**TF\_E\_NOOBJECT**</dt> <dt>0x80040202</dt></span></span> </dl>                                      | <span data-ttu-id="1f415-135">指定的位置不存在任何内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="1f415-135">No embedded object exists at the specified position.</span></span><br/>                                   |
| <span id="TF_E_NOPROVIDER"></span><span id="tf_e_noprovider"></span><dl> <span data-ttu-id="1f415-136"><dt>**TF \_E \_ NOPROVIDER**</dt> <dt>0x80040503</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-136"><dt>**TF\_E\_NOPROVIDER**</dt> <dt>0x80040503</dt></span></span> </dl>                                | <span data-ttu-id="1f415-137">指定的函式沒有函數提供者存在。</span><span class="sxs-lookup"><span data-stu-id="1f415-137">No function provider exists for the specified function.</span></span><br/>                                |
| <span id="TF_E_NOSELECTION"></span><span id="tf_e_noselection"></span><dl> <span data-ttu-id="1f415-138"><dt>**TF \_E \_ NOSELECTION**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-138"><dt>**TF\_E\_NOSELECTION**</dt> <dt>0x80040205</dt></span></span> </dl>                             | <span data-ttu-id="1f415-139">內容中不存在任何選取範圍。</span><span class="sxs-lookup"><span data-stu-id="1f415-139">No selection exists within the context.</span></span><br/>                                                |
| <span id="TF_E_NOSERVICE"></span><span id="tf_e_noservice"></span><dl> <span data-ttu-id="1f415-140"><dt>**TF \_E \_ NOSERVICE**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-140"><dt>**TF\_E\_NOSERVICE**</dt> <dt>0x80040203</dt></span></span> </dl>                                   | <span data-ttu-id="1f415-141">指定的服務不存在或無法建立。</span><span class="sxs-lookup"><span data-stu-id="1f415-141">The specified service does not exists or cannot be created.</span></span><br/>                            |
| <span id="TF_E_NOTOWNEDRANGE"></span><span id="tf_e_notownedrange"></span><dl> <span data-ttu-id="1f415-142"><dt>**TF \_E \_ NOTOWNEDRANGE**</dt> <dt>0x80040502</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-142"><dt>**TF\_E\_NOTOWNEDRANGE**</dt> <dt>0x80040502</dt></span></span> </dl>                       | <span data-ttu-id="1f415-143">TSF 管理員不會擁有此範圍。</span><span class="sxs-lookup"><span data-stu-id="1f415-143">The TSF manager does not own the range.</span></span><br/>                                                |
| <span id="TF_E_RANGE_NOT_COVERED"></span><span id="tf_e_range_not_covered"></span><dl> <span data-ttu-id="1f415-144"><dt>**TF \_E \_ 範圍 \_ 未 \_ 涵蓋**</dt> <dt>0x80040507</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-144"><dt>**TF\_E\_RANGE\_NOT\_COVERED**</dt> <dt>0x80040507</dt></span></span> </dl>         | <span data-ttu-id="1f415-145">範圍不在現用組合內。</span><span class="sxs-lookup"><span data-stu-id="1f415-145">The range is not within an active composition.</span></span><br/>                                         |
| <span id="TF_E_READONLY"></span><span id="tf_e_readonly"></span><dl> <span data-ttu-id="1f415-146"><dt>**TF \_E \_ READONLY**</dt> <dt>0x80040209</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-146"><dt>**TF\_E\_READONLY**</dt> <dt>0x80040209</dt></span></span> </dl>                                      | <span data-ttu-id="1f415-147">編輯內容是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1f415-147">The edit context is read-only.</span></span><br/>                                                         |
| <span id="TF_E_STACKFULL"></span><span id="tf_e_stackfull"></span><dl> <span data-ttu-id="1f415-148"><dt>**TF \_E \_ STACKFULL**</dt> <dt>0x80040501</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-148"><dt>**TF\_E\_STACKFULL**</dt> <dt>0x80040501</dt></span></span> </dl>                                   | <span data-ttu-id="1f415-149">內容堆疊已滿。</span><span class="sxs-lookup"><span data-stu-id="1f415-149">The context stack is full.</span></span><br/>                                                             |
| <span id="TF_E_SYNCHRONOUS"></span><span id="tf_e_synchronous"></span><dl> <span data-ttu-id="1f415-150"><dt>**TF \_E \_ 同步**</dt> <dt>0x80040208</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-150"><dt>**TF\_E\_SYNCHRONOUS**</dt> <dt>0x80040208</dt></span></span> </dl>                             | <span data-ttu-id="1f415-151">無法取得同步的唯讀鎖定。</span><span class="sxs-lookup"><span data-stu-id="1f415-151">A synchronous read-only lock cannot be obtained.</span></span><br/>                                       |
| <span id="TF_S_ASYNC"></span><span id="tf_s_async"></span><dl> <span data-ttu-id="1f415-152"><dt>**TF \_S \_ ASYNC**</dt> <dt>0x00040300</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-152"><dt>**TF\_S\_ASYNC**</dt> <dt>0x00040300</dt></span></span> </dl>                                               | <span data-ttu-id="1f415-153">資料將會以非同步方式取得。</span><span class="sxs-lookup"><span data-stu-id="1f415-153">The data will be obtained asynchronously.</span></span><br/>                                              |



 

## <a name="requirements"></a><span data-ttu-id="1f415-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f415-154">Requirements</span></span>



| <span data-ttu-id="1f415-155">需求</span><span class="sxs-lookup"><span data-stu-id="1f415-155">Requirement</span></span> | <span data-ttu-id="1f415-156">值</span><span class="sxs-lookup"><span data-stu-id="1f415-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f415-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f415-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1f415-158">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f415-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1f415-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f415-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1f415-160">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f415-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1f415-161">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1f415-161">Redistributable</span></span><br/>          | <span data-ttu-id="1f415-162">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="1f415-162">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="1f415-163">標頭</span><span class="sxs-lookup"><span data-stu-id="1f415-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f415-164"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-164"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f415-165">Idl</span><span class="sxs-lookup"><span data-stu-id="1f415-165">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f415-166"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f415-166"><dt>Msctf.idl</dt></span></span> </dl> |



 

 





