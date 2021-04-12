---
title: 'RPC_IF_HANDLE (Rpcdce) '
description: '\_如果 \_ 處理資料類型宣告介面控制碼，則為 RPC。'
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934840"
---
# <a name="rpc_if_handle"></a><span data-ttu-id="d0133-104">RPC \_ IF \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="d0133-104">RPC\_IF\_HANDLE</span></span>

<span data-ttu-id="d0133-105">**\_ 如果 \_ 處理** 資料類型宣告介面控制碼，則為 RPC。</span><span class="sxs-lookup"><span data-stu-id="d0133-105">The **RPC\_IF\_HANDLE** data type declares an interface handle.</span></span>


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="d0133-106">備註</span><span class="sxs-lookup"><span data-stu-id="d0133-106">Remarks</span></span>

<span data-ttu-id="d0133-107">RPC 執行時間程式庫會使用介面控制碼來存取介面規格資料結構。</span><span class="sxs-lookup"><span data-stu-id="d0133-107">The RPC run-time library uses interface handles to access the interface-specification data structure.</span></span> <span data-ttu-id="d0133-108">MIDL 編譯器會自動從每個 IDL 檔案建立介面規格資料結構，並在 \_ 介面規格的控制碼中建立 RPC 型別的全域變數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d0133-108">The MIDL compiler automatically creates an interface-specification data structure from each IDL file and creates a global variable of type RPC\_IF\_HANDLE for the interface specification.</span></span>

<span data-ttu-id="d0133-109">MIDL 編譯器會在針對介面產生的每個標頭檔中包含介面控制碼。</span><span class="sxs-lookup"><span data-stu-id="d0133-109">The MIDL compiler includes an interface handle in each header file generated for the interface.</span></span> <span data-ttu-id="d0133-110">需要介面規格做為參數的函式會顯示 RPC 的資料類型（ **\_ 如果是 \_ 控制碼**）。</span><span class="sxs-lookup"><span data-stu-id="d0133-110">Functions requiring the interface specification as a parameter show a data type of **RPC\_IF\_HANDLE**.</span></span> <span data-ttu-id="d0133-111">每個介面控制碼名稱的形式如下：</span><span class="sxs-lookup"><span data-stu-id="d0133-111">The form of each interface handle name is as follows:</span></span>

-   <span data-ttu-id="d0133-112">*if-name* \_用戶端) 的 ClientIfHandle (</span><span class="sxs-lookup"><span data-stu-id="d0133-112">*if-name*\_ClientIfHandle (for the client)</span></span>
-   <span data-ttu-id="d0133-113">*if-name* \_ServerIfHandle 伺服器) 的 (</span><span class="sxs-lookup"><span data-stu-id="d0133-113">*if-name*\_ServerIfHandle (for the server)</span></span>

<span data-ttu-id="d0133-114">*If-name* 部分指定 IDL 檔案中的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0133-114">The *if-name* part specifies the interface identifier in the IDL file.</span></span>

<span data-ttu-id="d0133-115">例如：</span><span class="sxs-lookup"><span data-stu-id="d0133-115">For example:</span></span>

<span data-ttu-id="d0133-116">hello \_ ClientIfHandle</span><span class="sxs-lookup"><span data-stu-id="d0133-116">hello\_ClientIfHandle</span></span>

<span data-ttu-id="d0133-117">hello \_ ServerIfHandle</span><span class="sxs-lookup"><span data-stu-id="d0133-117">hello\_ServerIfHandle</span></span>

> [!Note]  
> <span data-ttu-id="d0133-118">介面控制碼名稱的最大長度是31個字元。</span><span class="sxs-lookup"><span data-stu-id="d0133-118">The maximum length of the interface handle name is 31 characters.</span></span>

 

<span data-ttu-id="d0133-119">因為名稱的 " \_ ClientIfHandle" 和 " \_ ServerIfHandle" 部分需要15個字元，所以 *name* 元素的長度不能超過16個字元。</span><span class="sxs-lookup"><span data-stu-id="d0133-119">Because the "\_ClientIfHandle" and "\_ServerIfHandle" parts of the names require 15 characters, the *if-name* element can be no more than 16 characters long.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0133-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0133-120">Requirements</span></span>



| <span data-ttu-id="d0133-121">需求</span><span class="sxs-lookup"><span data-stu-id="d0133-121">Requirement</span></span> | <span data-ttu-id="d0133-122">值</span><span class="sxs-lookup"><span data-stu-id="d0133-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0133-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0133-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0133-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0133-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d0133-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0133-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0133-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0133-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d0133-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d0133-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0133-128"><dt>Rpcdce (包含 Rpc) </dt></span><span class="sxs-lookup"><span data-stu-id="d0133-128"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





