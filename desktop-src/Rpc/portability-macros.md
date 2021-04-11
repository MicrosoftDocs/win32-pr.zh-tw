---
title: '可攜性宏 (Rpc .h) '
description: RPC 工具藉由將產生的存根檔案和標頭檔中的資料類型與函式傳回型別與每個平臺特有的定義產生關聯，以達成模型、呼叫和命名慣例的獨立性。
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- 可攜性宏 RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "103945579"
---
# <a name="portability-macros"></a><span data-ttu-id="a0c98-104">可攜性宏</span><span class="sxs-lookup"><span data-stu-id="a0c98-104">Portability Macros</span></span>

<span data-ttu-id="a0c98-105">RPC 工具藉由將產生的存根檔案和標頭檔中的資料類型與函式傳回型別與每個平臺特有的定義產生關聯，以達成模型、呼叫和命名慣例的獨立性。</span><span class="sxs-lookup"><span data-stu-id="a0c98-105">The RPC tools achieve model, calling, and naming-convention independence by associating data types and function-return types in the generated stub files and header files with definitions that are specific to each platform.</span></span> <span data-ttu-id="a0c98-106">這些巨集定義可確保任何需要指定的資料類型和 **\_ \_ 函數都指定為目前的物件**。</span><span class="sxs-lookup"><span data-stu-id="a0c98-106">These macro definitions ensure that any data types and functions that require the designation of **\_\_far** are specified as far objects.</span></span>

<span data-ttu-id="a0c98-107">下圖顯示 MIDL 編譯器套用至 RPC 元件之間函式呼叫的巨集定義：</span><span class="sxs-lookup"><span data-stu-id="a0c98-107">The following figure shows the macro definitions that the MIDL compiler applies to function calls between RPC components:</span></span>

![顯示 MIDL 套用至函式呼叫之巨集定義的圖表。](images/prog-a29.png)

<span data-ttu-id="a0c98-109">RPC 宏的定義如下。</span><span class="sxs-lookup"><span data-stu-id="a0c98-109">RPC macros are defined as follows.</span></span>



| <span data-ttu-id="a0c98-110">定義</span><span class="sxs-lookup"><span data-stu-id="a0c98-110">Definition</span></span>    | <span data-ttu-id="a0c98-111">描述</span><span class="sxs-lookup"><span data-stu-id="a0c98-111">Description</span></span>                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0c98-112">\_\_RPC \_ API</span><span class="sxs-lookup"><span data-stu-id="a0c98-112">\_\_RPC\_API</span></span>  | <span data-ttu-id="a0c98-113">適用于存根對使用者應用程式所進行的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a0c98-113">Applied to calls made by the stub to the user application.</span></span> <span data-ttu-id="a0c98-114">這兩個函數都在相同的可執行程式中。</span><span class="sxs-lookup"><span data-stu-id="a0c98-114">Both functions are in the same executable program.</span></span>                                       |
| <span data-ttu-id="a0c98-115">\_\_目前的 RPC \_</span><span class="sxs-lookup"><span data-stu-id="a0c98-115">\_\_RPC\_FAR</span></span>  | <span data-ttu-id="a0c98-116">適用于指標的標準巨集定義。</span><span class="sxs-lookup"><span data-stu-id="a0c98-116">Applied to the standard macro definition for pointers.</span></span> <span data-ttu-id="a0c98-117">此巨集定義應該會顯示為所有使用者提供之函式簽章的一部分。</span><span class="sxs-lookup"><span data-stu-id="a0c98-117">This macro definition should appear as part of the signature of all user-supplied functions.</span></span> |
| <span data-ttu-id="a0c98-118">\_\_RPC \_ 存根</span><span class="sxs-lookup"><span data-stu-id="a0c98-118">\_\_RPC\_STUB</span></span> | <span data-ttu-id="a0c98-119">套用至從執行時間程式庫對存根進行的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a0c98-119">Applied to calls made from the run-time library to the stub.</span></span> <span data-ttu-id="a0c98-120">這些呼叫可視為私用。</span><span class="sxs-lookup"><span data-stu-id="a0c98-120">These calls can be considered private.</span></span>                                                 |
| <span data-ttu-id="a0c98-121">\_\_RPC \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="a0c98-121">\_\_RPC\_USER</span></span> | <span data-ttu-id="a0c98-122">適用于執行時間程式庫對使用者應用程式所進行的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a0c98-122">Applied to calls made by the run-time library to the user application.</span></span> <span data-ttu-id="a0c98-123">這些會跨越 DLL 和應用程式之間的界限。</span><span class="sxs-lookup"><span data-stu-id="a0c98-123">These cross the boundary between a DLL and an application.</span></span>                   |
| <span data-ttu-id="a0c98-124">RPC \_ 專案</span><span class="sxs-lookup"><span data-stu-id="a0c98-124">RPC\_ENTRY</span></span>    | <span data-ttu-id="a0c98-125">適用于應用程式或 stub 對執行時間程式庫所做的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a0c98-125">Applied to calls made by the application or stub to the run-time library.</span></span> <span data-ttu-id="a0c98-126">此巨集定義會套用至所有 RPC 執行時間函式。</span><span class="sxs-lookup"><span data-stu-id="a0c98-126">This macro definition is applied to all RPC run-time functions.</span></span>           |



 

<span data-ttu-id="a0c98-127">為了正確地連結 Microsoft RPC 執行時間程式庫、存根和支援常式，某些使用者提供的函式也必須在函式定義中包含這些宏。</span><span class="sxs-lookup"><span data-stu-id="a0c98-127">To link correctly with the Microsoft RPC run-time libraries, stubs, and support routines, some user-supplied functions must also include these macros in the function definition.</span></span> <span data-ttu-id="a0c98-128">當您定義與記憶體管理相關聯的函式、使用者定義的系結控制碼和 **傳輸 \_ 為** 屬性時，請使用宏 **\_ \_ rpc \_ API** ，並在定義與內容控制碼相關聯的內容執行常式時使用宏 **\_ \_ rpc \_ 使用者**。</span><span class="sxs-lookup"><span data-stu-id="a0c98-128">Use the macro **\_\_RPC\_API** when you define the functions associated with memory management, user-defined binding handles, and the **transmit\_as** attribute, and use the macro **\_\_RPC\_USER** when you define the context run-down routine associated with the context handle.</span></span> <span data-ttu-id="a0c98-129">將函數指定為：</span><span class="sxs-lookup"><span data-stu-id="a0c98-129">Specify the functions as:</span></span>

<dl> <dt>

<span data-ttu-id="a0c98-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC \_ 使用者 *midl \_ 使用者* \_ 配置 ( ... ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC\_USER *midl\_user*\_allocate(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC \_ 使用者 *midl \_ 使用者* \_ 可用 ( ... ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC\_USER *midl\_user*\_free(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC \_ 使用者 *handletype* \_ bind ( ... ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC\_USER  *handletype*\_bind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC \_ 使用者 *handletype* \_ 解除系結 ( ... ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC\_USER *handletype*\_unbind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC \_ 使用者 *類型* \_ 到 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="a0c98-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC\_USER *type*\_to\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_本機的 RPC 使用者 *類型* \_ \_</span><span class="sxs-lookup"><span data-stu-id="a0c98-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC\_USER *type*\_from\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_ \_ 要 xmit ( 的 RPC 使用者類型 ... \_ ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC\_USER type\_to\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_來自 xmit ( 的 RPC 使用者 *類型*... \_ \_ ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC\_USER *type*\_from\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC \_ 使用者 *類型* \_ 可用 \_ 本機</span><span class="sxs-lookup"><span data-stu-id="a0c98-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC\_USER *type*\_free\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC \_ 使用者 *類型* \_ free \_ inst ( ... ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC\_USER *type*\_free\_inst(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC \_ 使用者 *類型* \_ free \_ xmit ( ... ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC\_USER *type*\_free\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a0c98-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC \_ 使用者內容取消 \_ ( ... ) </span><span class="sxs-lookup"><span data-stu-id="a0c98-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC\_USER context\_rundown(...)</span></span>
<span data-ttu-id="a0c98-142"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a0c98-142"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="a0c98-143">這些函數中的所有指標參數都必須使用宏 **\_ \_ RPC \_** 來指定。</span><span class="sxs-lookup"><span data-stu-id="a0c98-143">All pointer parameters in these functions must be specified using the macro **\_\_RPC\_FAR**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0c98-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0c98-144">Requirements</span></span>



| <span data-ttu-id="a0c98-145">需求</span><span class="sxs-lookup"><span data-stu-id="a0c98-145">Requirement</span></span> | <span data-ttu-id="a0c98-146">值</span><span class="sxs-lookup"><span data-stu-id="a0c98-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a0c98-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0c98-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a0c98-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0c98-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a0c98-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0c98-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a0c98-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0c98-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a0c98-151">標頭</span><span class="sxs-lookup"><span data-stu-id="a0c98-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0c98-152"><dt>Rpc。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0c98-152"><dt>Rpc.h</dt></span></span> </dl> |



 

 





