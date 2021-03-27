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
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972341"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="30434-104">IShellFolderViewType：： GetDefaultViewName 方法</span><span class="sxs-lookup"><span data-stu-id="30434-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="30434-105">取得預設視圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="30434-105">Gets the name of the default view.</span></span> <span data-ttu-id="30434-106">呼叫 [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 以取得其他視圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="30434-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="30434-107">語法</span><span class="sxs-lookup"><span data-stu-id="30434-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="30434-108">參數</span><span class="sxs-lookup"><span data-stu-id="30434-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30434-109">*uFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30434-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30434-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="30434-110">Type: **DWORD**</span></span>

<span data-ttu-id="30434-111">選擇性旗標;應設定為0。</span><span class="sxs-lookup"><span data-stu-id="30434-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="30434-112">*ppwszName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="30434-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30434-113">類型： \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="30434-113">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="30434-114">接收預設視圖名稱之字串指標的位址。</span><span class="sxs-lookup"><span data-stu-id="30434-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="30434-115">字串的記憶體是使用 [_ *SHStrDup* \*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)來配置。</span><span class="sxs-lookup"><span data-stu-id="30434-115">The memory for the string is allocated with [_ *SHStrDup*\*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30434-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="30434-116">Return value</span></span>

<span data-ttu-id="30434-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30434-117">Type: **HRESULT**</span></span>

<span data-ttu-id="30434-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="30434-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30434-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="30434-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="30434-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="30434-120">Requirements</span></span>



| <span data-ttu-id="30434-121">需求</span><span class="sxs-lookup"><span data-stu-id="30434-121">Requirement</span></span> | <span data-ttu-id="30434-122">值</span><span class="sxs-lookup"><span data-stu-id="30434-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30434-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30434-123">Minimum supported client</span></span><br/> | <span data-ttu-id="30434-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30434-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="30434-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30434-125">Minimum supported server</span></span><br/> | <span data-ttu-id="30434-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30434-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="30434-127">DLL</span><span class="sxs-lookup"><span data-stu-id="30434-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30434-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30434-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




