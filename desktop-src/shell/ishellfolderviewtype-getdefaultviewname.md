---
description: 取得預設視圖的名稱。 呼叫 GetDisplayNameOf 以取得其他視圖的名稱。
title: IShellFolderViewType：： GetDefaultViewName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842759"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="e6655-104">IShellFolderViewType：： GetDefaultViewName 方法</span><span class="sxs-lookup"><span data-stu-id="e6655-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="e6655-105">取得預設視圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6655-105">Gets the name of the default view.</span></span> <span data-ttu-id="e6655-106">呼叫 [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 以取得其他視圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6655-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6655-107">語法</span><span class="sxs-lookup"><span data-stu-id="e6655-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="e6655-108">參數</span><span class="sxs-lookup"><span data-stu-id="e6655-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6655-109">*uFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6655-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6655-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6655-110">Type: **DWORD**</span></span>

<span data-ttu-id="e6655-111">選擇性旗標;應設定為0。</span><span class="sxs-lookup"><span data-stu-id="e6655-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e6655-112">*ppwszName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e6655-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6655-113">類型： **LPWSTR \***</span><span class="sxs-lookup"><span data-stu-id="e6655-113">Type: **LPWSTR\***</span></span>

<span data-ttu-id="e6655-114">接收預設視圖名稱之字串指標的位址。</span><span class="sxs-lookup"><span data-stu-id="e6655-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="e6655-115">使用 [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e6655-115">The memory for the string is allocated with [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6655-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6655-116">Return value</span></span>

<span data-ttu-id="e6655-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e6655-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e6655-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e6655-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6655-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e6655-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6655-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6655-120">Requirements</span></span>



| <span data-ttu-id="e6655-121">需求</span><span class="sxs-lookup"><span data-stu-id="e6655-121">Requirement</span></span> | <span data-ttu-id="e6655-122">值</span><span class="sxs-lookup"><span data-stu-id="e6655-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6655-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6655-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6655-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6655-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6655-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6655-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6655-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6655-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e6655-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e6655-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6655-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6655-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




