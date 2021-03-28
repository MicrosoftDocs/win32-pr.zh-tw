---
description: 重建專案識別碼清單的指標， (從 Shell 資料夾的一個階層式標記法轉換成不同的標記法，以 PIDL) 。
title: IShellFolderViewType：： TranslateViewPidl 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512201"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="dbc69-103">IShellFolderViewType：： TranslateViewPidl 方法</span><span class="sxs-lookup"><span data-stu-id="dbc69-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="dbc69-104">重建專案識別碼清單的指標， (從 Shell 資料夾的一個階層式標記法轉換成不同的標記法，以 PIDL) 。</span><span class="sxs-lookup"><span data-stu-id="dbc69-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc69-105">語法</span><span class="sxs-lookup"><span data-stu-id="dbc69-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="dbc69-106">參數</span><span class="sxs-lookup"><span data-stu-id="dbc69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc69-107">*pidl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dbc69-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc69-108">類型： **PCUIDLIST \_ 相對**</span><span class="sxs-lookup"><span data-stu-id="dbc69-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="dbc69-109">相對於根資料夾之專案識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="dbc69-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="dbc69-110">*pidlView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dbc69-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc69-111">類型： **PCUIDLIST \_ 相對**</span><span class="sxs-lookup"><span data-stu-id="dbc69-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="dbc69-112">視圖的特殊 PIDL。</span><span class="sxs-lookup"><span data-stu-id="dbc69-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="dbc69-113">*ppidlOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dbc69-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc69-114">類型： \**PCUIDLIST \_ 相對 \** _</span><span class="sxs-lookup"><span data-stu-id="dbc69-114">Type: \**PCUIDLIST\_RELATIVE\** _</span></span>

<span data-ttu-id="dbc69-115">要接收翻譯之 PIDL 變數的位址。</span><span class="sxs-lookup"><span data-stu-id="dbc69-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc69-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbc69-116">Return value</span></span>

<span data-ttu-id="dbc69-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dbc69-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dbc69-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="dbc69-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbc69-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dbc69-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc69-120">備註</span><span class="sxs-lookup"><span data-stu-id="dbc69-120">Remarks</span></span>

<span data-ttu-id="dbc69-121">完成時，您應該使用 [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree)釋放傳回的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="dbc69-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc69-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbc69-122">Requirements</span></span>



| <span data-ttu-id="dbc69-123">需求</span><span class="sxs-lookup"><span data-stu-id="dbc69-123">Requirement</span></span> | <span data-ttu-id="dbc69-124">值</span><span class="sxs-lookup"><span data-stu-id="dbc69-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc69-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbc69-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc69-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbc69-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dbc69-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbc69-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc69-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbc69-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dbc69-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dbc69-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbc69-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbc69-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




