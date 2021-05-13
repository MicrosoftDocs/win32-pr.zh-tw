---
description: 開始取消暫止之非同步搜尋的進程。
title: IShellFolderSearchable：： CancelAsyncSearch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842989"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="5e98e-103">IShellFolderSearchable：： CancelAsyncSearch 方法</span><span class="sxs-lookup"><span data-stu-id="5e98e-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="5e98e-104">開始取消暫止之非同步搜尋的進程。</span><span class="sxs-lookup"><span data-stu-id="5e98e-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e98e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5e98e-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5e98e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e98e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e98e-107">*pidlSearch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e98e-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e98e-108">類型： **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="5e98e-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="5e98e-109">搜尋 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 的指標。</span><span class="sxs-lookup"><span data-stu-id="5e98e-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="5e98e-110">*pdwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e98e-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e98e-111">類型： **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="5e98e-111">Type: **DWORD\***</span></span>

<span data-ttu-id="5e98e-112">目前未定義任何旗標;設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5e98e-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e98e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e98e-113">Return value</span></span>

<span data-ttu-id="5e98e-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e98e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5e98e-115">\_如果取消，則傳回 s OK; \_ 如果搜尋未執行，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="5e98e-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e98e-116">備註</span><span class="sxs-lookup"><span data-stu-id="5e98e-116">Remarks</span></span>

<span data-ttu-id="5e98e-117">實際取消搜尋時，會呼叫 [**RunEnd**](ishellfoldersearchablecallback-runend.md) 。</span><span class="sxs-lookup"><span data-stu-id="5e98e-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e98e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e98e-118">Requirements</span></span>



| <span data-ttu-id="5e98e-119">需求</span><span class="sxs-lookup"><span data-stu-id="5e98e-119">Requirement</span></span> | <span data-ttu-id="5e98e-120">值</span><span class="sxs-lookup"><span data-stu-id="5e98e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e98e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e98e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5e98e-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e98e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5e98e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e98e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5e98e-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e98e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5e98e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5e98e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e98e-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e98e-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




