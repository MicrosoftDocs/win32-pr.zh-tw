---
description: 表示搜尋已啟動。
title: IShellFolderSearchableCallback：： RunBegin 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 2bef0f29486143f97f886c0d31ab456a070ed857
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512204"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a><span data-ttu-id="95837-103">IShellFolderSearchableCallback：： RunBegin 方法</span><span class="sxs-lookup"><span data-stu-id="95837-103">IShellFolderSearchableCallback::RunBegin method</span></span>

<span data-ttu-id="95837-104">表示搜尋已啟動。</span><span class="sxs-lookup"><span data-stu-id="95837-104">Indicates that a search was started.</span></span>

## <a name="syntax"></a><span data-ttu-id="95837-105">語法</span><span class="sxs-lookup"><span data-stu-id="95837-105">Syntax</span></span>


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="95837-106">參數</span><span class="sxs-lookup"><span data-stu-id="95837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95837-107">*>dwreserved* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95837-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95837-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="95837-108">Type: **DWORD**</span></span>

<span data-ttu-id="95837-109">保留的。</span><span class="sxs-lookup"><span data-stu-id="95837-109">Reserved.</span></span> <span data-ttu-id="95837-110">必須設定為 0。</span><span class="sxs-lookup"><span data-stu-id="95837-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95837-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95837-111">Return value</span></span>

<span data-ttu-id="95837-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="95837-112">Type: **HRESULT**</span></span>

<span data-ttu-id="95837-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="95837-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95837-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="95837-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="95837-115">備註</span><span class="sxs-lookup"><span data-stu-id="95837-115">Remarks</span></span>

<span data-ttu-id="95837-116">例如，為了回應此回呼，應用程式可能會啟用 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="95837-116">In response to this callback, the application may enable the **Cancel** button, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="95837-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="95837-117">Requirements</span></span>



| <span data-ttu-id="95837-118">需求</span><span class="sxs-lookup"><span data-stu-id="95837-118">Requirement</span></span> | <span data-ttu-id="95837-119">值</span><span class="sxs-lookup"><span data-stu-id="95837-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95837-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95837-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95837-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95837-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="95837-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95837-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95837-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95837-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="95837-124">DLL</span><span class="sxs-lookup"><span data-stu-id="95837-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95837-125"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95837-125"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




